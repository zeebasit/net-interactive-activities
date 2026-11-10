# net-interactive-activities
Interactive learning activities for the Network Infrastructure course

## Engagement instrumentation for new activities

Existing activity pages load a shared, **privacy-gated** engagement script (installed but not active until an approved analytics service is connected). When creating a new HTML activity, include this tag just before the final actual `</body>` element:

```html
<script defer src="https://zeebasit.github.io/IIS-activities/shared/engagement.js" data-engagement-version="1"></script>
```

For activities with a clear finishing condition, call `window.ActivityEngagement?.complete()` after that condition is met. Never send student names, answers, scores or other identifying information as analytics properties.

See [Engagement setup, privacy and reporting](https://github.com/zeebasit/IIS-activities/blob/main/shared/ENGAGEMENT_SETUP.md) before enabling external data collection.
