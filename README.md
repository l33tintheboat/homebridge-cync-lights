# Homebridge Cync Lights by GE Plugin

This plugin integrates the Cync Direct Connect light bulbs from GE with Homekit.  These bulbs are very high quality and tolerate
the variations in voltage from power sources much better than many other bulbs on the market.  But GE has abandoned it's
support for Homekit in it's Cync products.

## Homebridge 2.0 Compatibility

This fork has been updated to support **Homebridge 2.0** and maintain backward compatibility with Homebridge 1.8.0+. The following changes were made:

- **ES Module Support**: Migrated to ES modules with proper `type: "module"` configuration and exports field for correct module resolution
- **Child Bridge Compatibility**: Fixed initialization order to prevent crashes when running as a child bridge (moved hub and API initialization to constructor body)
- **Package Configuration**: Added explicit `files` and `exports` fields to ensure proper package distribution
- **Engine Support**: Updated to support Node.js 18.17+, 20.9+, 22+, 24+, and 25+ with Homebridge 1.8.0+ or 2.0.0+
- **TypeScript Configuration**: Updated module resolution and target settings for modern Node.js compatibility

### Migrating from Original Plugin

If you're upgrading from the original `homebridge-cync-lights` plugin, the configuration remains the same. Simply:
1. Uninstall the old plugin: `npm uninstall -g homebridge-cync-lights`
2. Install this version: `npm install -g homebridge2-cync-lights`
3. Your existing configuration in `config.json` will continue to work

## Credits

- **Original Plugin**: Based on [homebridge-cync-lights](https://github.com/davidashman/homebridge-cync-lights) by David Ashman
- **Protocol Research**: Thanks to [nikshriv](https://github.com/nikshriv/cync_lights) and [unixpickle](https://github.com/unixpickle/cbyge) for your research and insights into the binary protocol