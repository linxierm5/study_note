# ContextWrapper
## 重写Context
``` java
@NonNull
private static Context getContext() {
   final Context baseContext = MyApplication.getContext();
   return new Context() {
      @Override
      public AssetManager getAssets() {
         return baseContext.getAssets();
      }

      @Override
      public Resources getResources() {
         return baseContext.getResources();
      }

      @Override
      public PackageManager getPackageManager() {
         return baseContext.getPackageManager();
      }

      @Override
      public ContentResolver getContentResolver() {
         return baseContext.getContentResolver();
      }

      @Override
      public Looper getMainLooper() {
         return baseContext.getMainLooper();
      }

      @Override
      public Context getApplicationContext() {
         return baseContext.getApplicationContext();
      }

      @Override
      public void setTheme(int resid) {
         baseContext.setTheme(resid);
      }

      @Override
      public Resources.Theme getTheme() {
         return baseContext.getTheme();
      }

      @Override
      public ClassLoader getClassLoader() {
         return baseContext.getClassLoader();
      }

      @Override
      public String getPackageName() {
         return "YourPackageName";
      }

      @Override
      public ApplicationInfo getApplicationInfo() {
         return baseContext.getApplicationInfo();
      }

      @Override
      public String getPackageResourcePath() {
         return baseContext.getPackageResourcePath();
      }

      @Override
      public String getPackageCodePath() {
         return baseContext.getPackageCodePath();
      }

      @Override
      public SharedPreferences getSharedPreferences(String name, int mode) {
         return baseContext.getSharedPreferences(name, mode);
      }

      @Override
      public boolean moveSharedPreferencesFrom(Context sourceContext, String name) {
         return false;
      }

      @Override
      public boolean deleteSharedPreferences(String name) {
         return false;
      }

      @Override
      public FileInputStream openFileInput(String name) throws FileNotFoundException {
         return baseContext.openFileInput(name);
      }

      @Override
      public FileOutputStream openFileOutput(String name, int mode) throws FileNotFoundException {
         return baseContext.openFileOutput(name, mode);
      }

      @Override
      public boolean deleteFile(String name) {
         return baseContext.deleteFile(name);
      }

      @Override
      public File getFileStreamPath(String name) {
         return baseContext.getFileStreamPath(name);
      }

      @Override
      public File getDataDir() {
         return null;
      }

      @Override
      public File getFilesDir() {
         return baseContext.getFilesDir();
      }

      @Override
      public File getNoBackupFilesDir() {
         return baseContext.getNoBackupFilesDir();
      }

      @Nullable
      @Override
      public File getExternalFilesDir(String type) {
         return baseContext.getExternalFilesDir(type);
      }

      @Override
      public File[] getExternalFilesDirs(String type) {
         return baseContext.getExternalFilesDirs(type);
      }

      @Override
      public File getObbDir() {
         return baseContext.getObbDir();
      }

      @Override
      public File[] getObbDirs() {
         return baseContext.getObbDirs();
      }

      @Override
      public File getCacheDir() {
         return baseContext.getCacheDir();
      }

      @Override
      public File getCodeCacheDir() {
         return baseContext.getCodeCacheDir();
      }

      @Nullable
      @Override
      public File getExternalCacheDir() {
         return baseContext.getExternalCacheDir();
      }

      @Override
      public File[] getExternalCacheDirs() {
         return baseContext.getExternalCacheDirs();
      }

      @Override
      public File[] getExternalMediaDirs() {
         return baseContext.getExternalMediaDirs();
      }

      @Override
      public String[] fileList() {
         return baseContext.fileList();
      }

      @Override
      public File getDir(String name, int mode) {
         return baseContext.getDir(name, mode);
      }

      @Override
      public SQLiteDatabase openOrCreateDatabase(String name, int mode, SQLiteDatabase.CursorFactory factory) {
         return baseContext.openOrCreateDatabase(name, mode, factory);
      }

      @Override
      public SQLiteDatabase openOrCreateDatabase(String name, int mode, SQLiteDatabase.CursorFactory factory, DatabaseErrorHandler errorHandler) {
         return baseContext.openOrCreateDatabase(name, mode, factory, errorHandler);
      }

      @Override
      public boolean moveDatabaseFrom(Context sourceContext, String name) {
         return false;
      }

      @Override
      public boolean deleteDatabase(String name) {
         return baseContext.deleteFile(name);
      }

      @Override
      public File getDatabasePath(String name) {
         return baseContext.getDatabasePath(name);
      }

      @Override
      public String[] databaseList() {
         return baseContext.databaseList();
      }

      @Override
      public Drawable getWallpaper() {
         return baseContext.getWallpaper();
      }

      @Override
      public Drawable peekWallpaper() {
         return baseContext.peekWallpaper();
      }

      @Override
      public int getWallpaperDesiredMinimumWidth() {
         return baseContext.getWallpaperDesiredMinimumWidth();
      }

      @Override
      public int getWallpaperDesiredMinimumHeight() {
         return baseContext.getWallpaperDesiredMinimumHeight();
      }

      @Override
      public void setWallpaper(Bitmap bitmap) throws IOException {
         baseContext.setWallpaper(bitmap);
      }

      @Override
      public void setWallpaper(InputStream data) throws IOException {
         baseContext.setWallpaper(data);
      }

      @Override
      public void clearWallpaper() throws IOException {
         baseContext.clearWallpaper();
      }

      @Override
      public void startActivity(Intent intent) {
         baseContext.startActivity(intent);
      }

      @Override
      public void startActivity(Intent intent, Bundle options) {
         baseContext.startActivity(intent, options);
      }

      @Override
      public void startActivities(Intent[] intents) {
         baseContext.startActivities(intents);
      }

      @Override
      public void startActivities(Intent[] intents, Bundle options) {
         baseContext.startActivities(intents, options);
      }

      @Override
      public void startIntentSender(IntentSender intent, Intent fillInIntent, int flagsMask, int flagsValues, int extraFlags) throws IntentSender.SendIntentException {
         baseContext.startIntentSender(intent, fillInIntent, flagsMask, flagsValues, extraFlags);
      }

      @Override
      public void startIntentSender(IntentSender intent, Intent fillInIntent, int flagsMask, int flagsValues, int extraFlags, Bundle options) throws IntentSender.SendIntentException {
         baseContext.startIntentSender(intent, fillInIntent, flagsMask, flagsValues, extraFlags, options);
      }

      @Override
      public void sendBroadcast(Intent intent) {
         baseContext.sendBroadcast(intent);
      }

      @Override
      public void sendBroadcast(Intent intent, String receiverPermission) {
         baseContext.sendBroadcast(intent, receiverPermission);
      }

      @Override
      public void sendOrderedBroadcast(Intent intent, String receiverPermission) {
         baseContext.sendOrderedBroadcast(intent, receiverPermission);
      }

      @Override
      public void sendOrderedBroadcast(Intent intent, String receiverPermission, BroadcastReceiver resultReceiver, Handler scheduler, int initialCode, String initialData, Bundle initialExtras) {
         baseContext.sendOrderedBroadcast(intent, receiverPermission, resultReceiver, scheduler, initialCode, initialData, initialExtras);
      }

      @Override
      public void sendBroadcastAsUser(Intent intent, UserHandle user) {
         baseContext.sendBroadcastAsUser(intent, user);
      }

      @Override
      public void sendBroadcastAsUser(Intent intent, UserHandle user, String receiverPermission) {
         baseContext.sendBroadcastAsUser(intent, user, receiverPermission);
      }

      @Override
      public void sendOrderedBroadcastAsUser(Intent intent, UserHandle user, String receiverPermission, BroadcastReceiver resultReceiver, Handler scheduler, int initialCode, String initialData, Bundle initialExtras) {
         baseContext.sendOrderedBroadcastAsUser(intent, user, receiverPermission, resultReceiver, scheduler, initialCode, initialData, initialExtras);
      }

      @Override
      public void sendStickyBroadcast(Intent intent) {
         baseContext.sendStickyBroadcast(intent);
      }

      @Override
      public void sendStickyOrderedBroadcast(Intent intent, BroadcastReceiver resultReceiver, Handler scheduler, int initialCode, String initialData, Bundle initialExtras) {
         baseContext.sendStickyOrderedBroadcast(intent, resultReceiver, scheduler, initialCode, initialData, initialExtras);
      }

      @Override
      public void removeStickyBroadcast(Intent intent) {
         baseContext.removeStickyBroadcast(intent);
      }

      @Override
      public void sendStickyBroadcastAsUser(Intent intent, UserHandle user) {
         baseContext.sendStickyBroadcastAsUser(intent, user);
      }

      @Override
      public void sendStickyOrderedBroadcastAsUser(Intent intent, UserHandle user, BroadcastReceiver resultReceiver, Handler scheduler, int initialCode, String initialData, Bundle initialExtras) {
         baseContext.sendStickyOrderedBroadcastAsUser(intent, user, resultReceiver, scheduler, initialCode, initialData, initialExtras);
      }

      @Override
      public void removeStickyBroadcastAsUser(Intent intent, UserHandle user) {
         baseContext.removeStickyBroadcastAsUser(intent, user);
      }

      @Nullable
      @Override
      public Intent registerReceiver(BroadcastReceiver receiver, IntentFilter filter) {
         return baseContext.registerReceiver(receiver, filter);
      }

      @Nullable
      @Override
      public Intent registerReceiver(BroadcastReceiver receiver, IntentFilter filter, String broadcastPermission, Handler scheduler) {
         return baseContext.registerReceiver(receiver, filter, broadcastPermission, scheduler);
      }

      @Override
      public void unregisterReceiver(BroadcastReceiver receiver) {
         baseContext.unregisterReceiver(receiver);
      }

      @Nullable
      @Override
      public ComponentName startService(Intent service) {
         return baseContext.startService(service);
      }

      @Override
      public boolean stopService(Intent service) {
         return baseContext.stopService(service);
      }

      @Override
      public boolean bindService(Intent service, ServiceConnection conn, int flags) {
         return baseContext.bindService(service, conn, flags);
      }

      @Override
      public void unbindService(ServiceConnection conn) {
         baseContext.unbindService(conn);
      }

      @Override
      public boolean startInstrumentation(ComponentName className, String profileFile, Bundle arguments) {
         return baseContext.startInstrumentation(className, profileFile, arguments);
      }

      @Override
      public Object getSystemService(String name) {
         return baseContext.getSystemService(name);
      }

      @Override
      public String getSystemServiceName(Class<?> serviceClass) {
         return baseContext.getSystemServiceName(serviceClass);
      }

      @Override
      public int checkPermission(String permission, int pid, int uid) {
         return baseContext.checkPermission(permission, pid, uid);
      }

      @Override
      public int checkCallingPermission(String permission) {
         return baseContext.checkCallingPermission(permission);
      }

      @Override
      public int checkCallingOrSelfPermission(String permission) {
         return baseContext.checkCallingOrSelfPermission(permission);
      }

      @Override
      public int checkSelfPermission(String permission) {
         return baseContext.checkSelfPermission(permission);
      }

      @Override
      public void enforcePermission(String permission, int pid, int uid, String message) {
         baseContext.enforcePermission(permission, pid, uid, message);
      }

      @Override
      public void enforceCallingPermission(String permission, String message) {
         baseContext.enforceCallingPermission(permission, message);
      }

      @Override
      public void enforceCallingOrSelfPermission(String permission, String message) {
         baseContext.enforceCallingOrSelfPermission(permission, message);
      }

      @Override
      public void grantUriPermission(String toPackage, Uri uri, int modeFlags) {
         baseContext.grantUriPermission(toPackage, uri, modeFlags);
      }

      @Override
      public void revokeUriPermission(Uri uri, int modeFlags) {
         baseContext.revokeUriPermission(uri, modeFlags);
      }

      @Override
      public int checkUriPermission(Uri uri, int pid, int uid, int modeFlags) {
         return baseContext.checkUriPermission(uri, pid, uid, modeFlags);
      }

      @Override
      public int checkCallingUriPermission(Uri uri, int modeFlags) {
         return baseContext.checkCallingUriPermission(uri, modeFlags);
      }

      @Override
      public int checkCallingOrSelfUriPermission(Uri uri, int modeFlags) {
         return baseContext.checkCallingOrSelfUriPermission(uri, modeFlags);
      }

      @Override
      public int checkUriPermission(Uri uri, String readPermission, String writePermission, int pid, int uid, int modeFlags) {
         return checkUriPermission(uri, readPermission, writePermission, pid, uid, modeFlags);
      }

      @Override
      public void enforceUriPermission(Uri uri, int pid, int uid, int modeFlags, String message) {
         baseContext.enforceUriPermission(uri, pid, uid, modeFlags, message);
      }

      @Override
      public void enforceCallingUriPermission(Uri uri, int modeFlags, String message) {
         baseContext.enforceCallingUriPermission(uri, modeFlags, message);
      }

      @Override
      public void enforceCallingOrSelfUriPermission(Uri uri, int modeFlags, String message) {
         baseContext.enforceCallingOrSelfUriPermission(uri, modeFlags, message);
      }

      @Override
      public void enforceUriPermission(Uri uri, String readPermission, String writePermission, int pid, int uid, int modeFlags, String message) {
         baseContext.enforceUriPermission(uri, readPermission, writePermission, pid, uid, modeFlags, message);
      }

      @Override
      public Context createPackageContext(String packageName, int flags) throws PackageManager.NameNotFoundException {
         return baseContext.createPackageContext(packageName, flags);
      }

      @Override
      public Context createConfigurationContext(Configuration overrideConfiguration) {
         return baseContext.createConfigurationContext(overrideConfiguration);
      }

      @Override
      public Context createDisplayContext(Display display) {
         return baseContext.createDisplayContext(display);
      }

      @Override
      public Context createDeviceProtectedStorageContext() {
         return null;
      }

      @Override
      public boolean isDeviceProtectedStorage() {
         return false;
      }
   };
}
````



