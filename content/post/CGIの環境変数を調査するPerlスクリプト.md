+++
author = "Masayuki Ariki"
comments = true
date = "2016-05-04T17:37:57+09:00"
draft = false
image = ""
menu = ""
share = true
slug = "post-title"
tags = ""
title = "CGIの環境変数を調査するPerlスクリプト"

+++

レンタルサーバなどで環境変数を調査するPerlスクリプト

	#!/usr/local/bin/perl

	print "Content-type: text/html", "\n\n";

	print "<HTML><BODY>", "\n";
	print "<H1>環境変数</H1><HR>", "\n";

	foreach my $key( keys %ENV ){
	    print "$key: $ENV{$key}<BR>", "\n";
	}

	print "<HR>", "\n";
	print "</BODY></HTML>", "\n";

上記の内容を「env.cgi」のようなファイル名で保存し、サーバへアップします。Perlのパスについては、レンタルサーバの環境に合わせ、実行権についても、サーバ指定の権限を設定する必要があります。。設置したファイルへブラウザでアクセスすれば、環境変数が表示されます。