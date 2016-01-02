打 * 号为未测试过。

1. [qmlparticleeditor](https://github.com/wearyinside/qmlparticleeditor)

    > 纯 QML 编写的粒子可视编辑器。

2. [cloudmusicqt](https://github.com/SunRain/cloudmusicqt) *

    > 使用 Qt 制作的网易云音乐。有使用 QML 哦~

2. [CleanPlayer](https://github.com/pansinm/CleanPlayer) *

     > 百度音乐API，但是界面是仿制网易云的。

3. [qmlStyle](https://github.com/SunRain/qmlStyle)

    > DragBar 实现QQ列表界面侧划效果

    > ColorPalette 对于又可以换肤，每种皮肤下又可换多种颜色的一种实现策略

    > IOS-RadioButton 仿照ios开关按钮效果

    > LockscreenShortcut 仿小米锁屏4界面方向快捷键

4. [quickandroid](https://github.com/benlau/quickandroid) *

    > QML Material Design Component and Support Library for Android

5. [qzxing](https://github.com/dplanella/qzxing)

    > Qt 封装的 zxing 库。在windows 7 上可以很好的和 QML 的相机工作，但是在安卓上，有些许问题，例如，在我的魅蓝 note2 上，Camera 无法调整焦距，导致图像模糊，识别二维码失败。


6. [tbclient](https://github.com/yeatse/tbclient)

    > 夜切大大的百度贴吧 Qt 版，可以运行再塞班和 N9 上，里面一些 QML 设计手机应用的技巧可以使用到。（即使是三年前的 QML 代码现在看来还是很有用的。）


7. [QmlExplorer](https://github.com/surfsky/QmlExplorer)

    > 隐约记得是针对 QML 的扩展。

8. [Qute Launcher](https://github.com/Iktwo/QuteLauncher) *

    > 貌似是一个启动器？

10. [Bacon2D ](https://github.com/Bacon2D/Bacon2D) *

    > Bacon2D is a framework to ease 2D game development, providing ready-to-use QML  components useful for creating compeling games.

11. [sqlite-editor-qtqml](https://github.com/ndesai/sqlite-editor-qtqml) *

    > 使用 QML 作为界面的数据库软件。

12. [musicgear](https://github.com/Iktwo/musicgear)

    > QML on Android，有使用到 Java 的下载类，可以研究一番。

    > [MusicGear](https://github.com/Iktwo/musicgear/blob/master/android/src/com/iktwo/musicgear/MusicGear.java) 这个类有许多用的代码，可以给 Qt 应用交互使用。

    ```
    public static void download(String url, String name)
    {
        Log.v(TAG, "download(" + url + ", " + name + ")");

        dm = (DownloadManager) m_instance.getSystemService(DOWNLOAD_SERVICE);
        Request request = new Request(Uri.parse(url));
        request.setTitle(name);
        request.setDescription(url);
        request.allowScanningByMediaScanner();
        request.setNotificationVisibility(Request.VISIBILITY_VISIBLE_NOTIFY_COMPLETED);
        request.setDestinationInExternalPublicDir(Environment.DIRECTORY_MUSIC, name + ".mp3");
        dm.enqueue(request);
    }

    public static void share(String name, String url)
    {
        Intent share = new Intent(android.content.Intent.ACTION_SEND);
        share.setType("text/plain");
        share.addFlags(Intent.FLAG_ACTIVITY_CLEAR_WHEN_TASK_RESET);
        share.putExtra(Intent.EXTRA_SUBJECT, name);
        if (!name.isEmpty()) {
            share.putExtra(Intent.EXTRA_TEXT, name + " - " + url + " via Musicgear");
            m_instance.startActivity(Intent.createChooser(share, "Share " + name));
        } else {
            share.putExtra(Intent.EXTRA_TEXT, url + " via Musicgear");
            m_instance.startActivity(Intent.createChooser(share, "Share this music"));
        }

    }

    public static void toast(final String message)
    {
        m_instance.runOnUiThread(new Runnable() {
            public void run() {
                Toast.makeText(m_instance.getApplicationContext(), message, Toast.LENGTH_SHORT).show();
            }
        });
    }

    ```

13. [qt-creator-quick2-template](https://github.com/Iktwo/qt-creator-quick2-template) *

    > 项目模板

14. [material](https://github.com/rschiang/material) *

    > 纯 QML 实现的 material 风格控件。

15. [codesnippets-joona](https://github.com/jpetrell/codesnippets-joona)

    Code snippets for UI programming blog http://www.joona.net

    QtQuick 的 UI 编程