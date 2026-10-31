# 1. Clear out the system's extended quarantine attributes from the app bundle
xattr -cr "/Applications/MQTT Explorer.app"

# 2. Force an ad-hoc re-signature specifically using your configured bundle ID
codesign --force --deep --sign - --identifier de.t7n.apps.mqtt-explorer "/Applications/MQTT Explorer.app"
