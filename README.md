SentryAppender.Core
=============

[log4net](http://logging.apache.org/log4net/) appender to send errors to [Sentry](http://www.getsentry.com/).

Configure in app.config:

```xml
<log4net>
	<root>
		<level value="DEBUG" />
		<appender-ref ref="SentryAppender" />
	</root>
	<appender name="SentryAppender" type="SharpRaven.Log4Net.Core.SentryAppender, SharpRaven.Log4Net.Core">
		<DSN value="DSN_FROM_SENTRY_UI" />
		<Logger value="LOGGER_NAME" />
		<threshold value="ERROR" />
		<layout type="log4net.Layout.PatternLayout">
			<conversionPattern value="%5level - %message%newline" />
		</layout>
	</appender>
</log4net>
```

Install-Package SharpRaven.Log4Net.Core

dotnet add package SharpRaven.Log4Net.Core
