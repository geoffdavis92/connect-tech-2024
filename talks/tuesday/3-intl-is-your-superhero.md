# Intl is your superhero
*Raymond Cameron*

* About
  * Sr Dev Evangelist for Adobe
  * raymondcamden.com
  * raymondcamden@gmail.com
  * https://github.com/cfjedimaster/intl-is-your-superhero
* What is Intl
  * Namespace object
  * Aka it comprises of multiple functions
  * Supports i18n numbers/dates/strings/locale-specific string comparison + more!
  * Intl spec 
  * Very well supported
* What it's not
  * Translation
  * i18n of UI
  * Currency exchange
* General Syntax
  * `new Intl.<method>`
  * Default locale is user's locale
  * Locales can be string or object
  * Browser tries best based on input
* User's language
  * `navigator.language`
  * `navigator.languages`
  * `Accept-Language` header (but client-side JS can't read HTTP req headers)
  * NOT to do
    * user's IP language
* Date Formatting
  * `Intl.DateTimeFormat`
  * Format ranges; dates, times or both
  * Multiple baked in styles
  * Some options
    * Locale
    * Calendar and numbering system
    * 24hr (overrides locale)
    * Timezones
    * Day period
    * fractionalSecondDigits
    * Styles of date and time
* Date Rage formatting
  * displays range between 2 dates
* Relative date formatting
  * Intl.RelativeTimeFormatting
  * Describing time in past/future
  * ex: 3 days ago
  * Supports number and unit
* Cool, but how to pick units
* Duration Date formatting
  * Describes span of time
  * Intl.DurationFormat
  * Months down to nanoseconds
  * Formatting for different parts
  * >> Not supported in Firefox <<
* Number formatting
  * Intl.NumberFormat
  * Supports units, ranges
* Decimal options
  * minimumIntegerDigits
  * Different options for rounding
  * trailingZero
* Currency formatting
  * Currency symbols, location
  * Commas vs periods
* String stuff
* List formatting
  * Intl.ListFormat
  * Formats a list of items
  * Supports AND/OR, or no and/or ex (1,2, and 3; 1, 2, or 3; 1, 2, 3)
  * Pass array of strings
* Plural formatting
  * Intl.PluralRules
  * API will tell you which to use
  * Returns:
    * zero
    * one
    * two
    * few
    * many
    * other
  * Cardinal or ordinal types
* Segmentor
  * Intl.Segmentor
* Docs
  * MDN Intl docs
  * intl-explorer.com
  
