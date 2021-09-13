---
title: Touch events (Mozilla experimental)
slug: Web/API/Touch_events/Mozilla_experimental_events
tags:
  - DOM
  - Gecko DOM Reference
  - events
---
<div class="notecard warning">
  <p><strong>Warning:</strong> This experimental API was removed in Gecko 18.0 {{ geckoRelease("18.0") }}, when support for the standard touch events was implemented.</p>
</div>

<p>The experimental touch events API described on this page was available from Gecko 2.0 {{ geckoRelease("2.0") }} to Gecko/Firefox 17. You should instead use the <a href="/en-US/docs/Web/API/Touch_events">standard touch events API</a>, supported since Gecko/Firefox 6 with multi-touch support added in Gecko/Firefox 12.</p>

<p>This API allowed you to track the movement of the user's finger on a touch screen, monitoring the raw touch events generated by the system. Although touch events were based on — and work similarly to — mouse events, each event included an identifier that allowed you to track multiple fingers moving on the screen at the same time.</p>

<h2 id="Event_fields">Event fields</h2>

<p>Touch events were based upon {{domxref("MouseEvent")}}, and thereby shared all mouse event fields. They included one additional field.</p>
<dl>
  <dt>
    streamId</dt>
  <dd>
    A unique integer identifying the finger generating the event. When the <code>MozTouchDown</code> event is built, a unique value is assigned to that finger. Corresponding <code>MozTouchMove</code> and <code>MozTouchUp</code> events for that finger will have the same streamId value. This lets you track each finger's movements on the touch screen independently. The stream ID is unique until the <code>MozTouchUp</code> event occurs; after that, the value may be recycled for another series of events.</dd>
</dl>

<h2 id="Types_of_touch_events">Types of touch events</h2>
<dl>
  <dt>
    MozTouchDown</dt>
  <dd>
    Sent when the user begins a screen touch action.</dd>
  <dt>
    MozTouchMove</dt>
  <dd>
    Sent when the user moves his finger on the touch screen.</dd>
  <dt>
    MozTouchUp</dt>
  <dd>
    Sent when the user lifts his finger off the screen.</dd>
</dl>