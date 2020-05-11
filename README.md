# icecast-privatepatches

 my private patches for icecast.

## File List

* icecast-2.4.5-2.4.5.1.diff

  * return value of SSL_write() may be caught correctly in `src/connection.c` . It was not taken into account on icecast-2.4.5 .

  * based on [icecast 2.4.5 (gitlab)](https://gitlab.xiph.org/xiph/icecast-server/-/tree/release-2.4.5)

  * [notice] This versioning rule is unofficial.

* icecast-2.4.4-2.4.5.1.diff
  * return value of SSL_read() and SSL_write() are caught correctly in `src/connection.c` . See: [Issues #2355](https://gitlab.xiph.org/xiph/icecast-server/-/issues/2355)

  * `doc/config-file.html` was changed. See: [Issues #2362](https://gitlab.xiph.org/xiph/icecast-server/-/issues/2362)

  * based on [icecast 2.4.4 (released version)](https://xiph.org/downloads/)

* icecast-2.4.4-removeadminlink.diff

  * The `admin` link may not be necessary for pure listner.

* icecast-2.4.4-movelistenerurl.diff

  * `http://localhost:port/` is not used. Please access `http://localhost:port/listener/`.

  * This is one of the ways to avoid crawlers.

  * Because `status.xsl` is fixed, we can't hide the listener page from humans.
