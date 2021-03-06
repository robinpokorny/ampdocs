---
$title: เค้าโครงที่รองรับ
---


ทำให้องค์ประกอบต่างๆ เป็นแบบตอบสนองตามอุปกรณ์
โดยใส่ `layout=responsive`

[TOC]

## ค่าที่ใช้ได้สำหรับแอตทริบิวต์เค้าโครง

โดยค่าเริ่มต้น
ให้ใช้เค้าโครงแบบตอบสนองตามอุปกรณ์

รายการค่าที่ใช้ได้ทั้งหมดสำหรับแอตทริบิวต์เค้าโครงมีดังนี้

<table>
  <thead>
    <tr>
      <th class="col-twenty" data-th="Layout type">ประเภทเค้าโครง</th>
      <th class="col-twenty" data-th="Width/height required">ต้องระบุความกว้าง/ความสูง</th>
      <th data-th="Behavior">พฤติกรรม</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>nodisplay</code></td>
      <td class="col-twenty" data-th="Description">ไม่</td>
      <td data-th="Behavior">ไม่แสดงองค์ประกอบ เค้าโครงประเภทนี้ใช้กับองค์ประกอบ AMP ได้ทั้งหมด คอมโพเนนต์นี้ไม่กินเนื้อที่บนหน้าจอราวกับว่าไม่มีสไตล์การแสดงผล โดยจะสมมติว่าองค์ประกอบสามารถแสดงตัวมันเองได้เมื่อผู้ใช้มีการดำเนินการ ตัวอย่างเช่น <a href="/docs/reference/extended/amp-lightbox.html"><code>amp-lightbox</code></a></td>
    </tr>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>คงที่</code></td>
      <td class="col-twenty" data-th="Description">ใช่</td>
      <td data-th="Behavior">องค์ประกอบมีความกว้างและความสูงคงที่โดยไม่รองรับการตอบสนองตามอุปกรณ์ แต่จะยกเว้นเฉพาะองค์ประกอบ <a href="/docs/reference/amp-pixel.html"><code>amp-pixel</code></a> และ <a href="/docs/reference/extended/amp-audio.html"><code>amp-audio</code></a></td>
    </tr>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>ตอบสนองตามอุปกรณ์</code></td>
      <td class="col-twenty" data-th="Description">ใช่</td>
      <td data-th="Behavior">องค์ประกอบจะปรับขนาดให้พอดีกับความกว้างขององค์ประกอบคอนเทนเนอร์ของตัวเอง และปรับความสูงตามอัตราส่วนที่กำหนดโดยแอตทริบิวต์ความกว้างและความสูงโดยอัตโนมัติ เค้าโครงนี้ทำงานได้ดีมากสำหรับองค์ประกอบ AMP ส่วนใหญ่ ซึ่งรวมถึง <a href="/docs/reference/amp-img.html"><code>amp-img</code></a>, <a href="/docs/reference/amp-video.html"><code>amp-video</code></a> เนื้อที่ที่ใช้ได้ขึ้นอยู่กับองค์ประกอบระดับบนสุดและยังปรับแต่งได้โดยใช้ CSS <code>max-width</code></td>
    </tr>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>ความสูงคงที่</code></td>
      <td class="col-twenty" data-th="Description">ความสูงเท่านั้น</td>
      <td data-th="Behavior">องค์ประกอบกินเนื้อที่ที่มีให้ใช้ แต่คงความสูงไว้เท่าเดิม เค้าโครงนี้ทำงานได้ดีสำหรับองค์ประกอบอย่างเช่น <a href="/docs/reference/extended/amp-carousel.html"><code>amp-carousel</code></a> ที่เกี่ยวข้องกับเนื้อหาที่อยู่ในตำแหน่งแนวนอน แอตทริบิวต์ <code>width</code> ต้องไม่แสดงอยู่ หรือต้องเท่ากับ <code>auto</code></td>
    </tr>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>เติม</code></td>
      <td class="col-twenty" data-th="Description">ไม่</td>
      <td data-th="Behavior">องค์ประกอบกินเนื้อที่ที่มีให้ใช้ ทั้งความกว้างและความสูง กล่าวอีกอย่างหนึ่งคือ เค้าโครงขององค์ประกอบแบบเติมจะตรงกับองค์ประกอบระดับบนสุดของมัน</td>
    </tr>
    <tr>
      <td class="col-twenty" data-th="Layout type"><code>คอนเทนเนอร์</code></td>
      <td class="col-twenty" data-th="Description">ไม่</td>
      <td data-th="Behavior">องค์ประกอบอนุญาตให้องค์ประกอบระดับย่อยของตัวเองกำหนดขนาดได้ ซึ่งคล้ายกับ <code>div</code> ของ HTML ตามปกติ โดยสมมติว่าคอมโพเนนต์นั้นไม่มีเค้าโครงที่เฉพาะเจาะจงแต่ทำหน้าที่เป็นคอนเทนเนอร์เท่านั้น องค์ประกอบระดับย่อยขององค์ประกอบนี้จะแสดงผลทันที</td>
    </tr>
  </tbody>
</table>

### จะเกิดอะไรขึ้นถ้าไม่ได้กำหนดความกว้างและความสูงไว้

ในบางกรณี ถ้าไม่ได้ระบุ `width` หรือ `height` ไว้
รันไทม์ของ AMP สามารถกำหนดค่าเริ่มต้นให้กับค่าเหล่านี้ได้ดังนี้

* [`amp-pixel`](/docs/reference/amp-pixel.html): ทั้งความกว้างและความสูงมีค่าเริ่มต้นเป็น 0
* [`amp-audio`](/docs/reference/extended/amp-audio.html): ความกว้างและความสูงเริ่มต้นจะอนุมานจากเบราว์เซอร์

### จะเกิดอะไรขึ้นถ้าไม่ได้กำหนดแอตทริบิวต์เค้าโครงไว้

ระบบจะกำหนดพฤติกรรมของเค้าโครงดังนี้

* หาก `height` แสดงอยู่ และ `width` ไม่มีหรือเท่ากับ `auto` จะสมมติว่าใช้เค้าโครง `fixed-height`
* หากแอตทริบิวต์ `width` หรือ `height` แสดงอยู่พร้อมกับแอตทริบิวต์ `sizes` จะสมมติว่าใช้เค้าโครง `responsive`
* หากแอตทริบิวต์ `width` หรือ `height` แสดงอยู่ จะสมมติว่าใช้เค้าโครง `fixed`
* หาก `width` และ `height` ไม่ได้แสดงอยู่ จะสมมติว่าใช้เค้าโครง `container`

## การใช้ @media และสื่อ

ใช้ [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)
เพื่อควบคุมลักษณะและพฤติกรรมของเค้าโครงหน้าเว็บเช่นเดียวกับที่คุณทำกับเว็บไซต์อื่นๆ
เมื่อขนาดหรือการวางแนวของหน้าต่างเบราว์เซอร์เปลี่ยนแปลง
ระบบจะประเมินคำค้นหาตามสื่ออีกครั้ง ตลอดจนซ่อนและแสดงองค์ประกอบ
โดยอิงตามผลการค้นหาใหม่ๆ

เรียนรู้เพิ่มเติมเกี่ยวกับการควบคุมเค้าโครงโดยใช้คำค้นหาตามสื่อใน
[ใช้คำค้นหาตามสื่อของ CSS สำหรับการตอบสนองตามอุปกรณ์](https://developers.google.com/web/fundamentals/design-and-ui/responsive/fundamentals/use-media-queries?hl=en)

คุณลักษณะพิเศษอย่างหนึ่งสำหรับการออกแบบที่ตอบสนองตามอุปกรณ์ที่มีให้ใช้งานใน AMP คือแอตทริบิวต์ `media`
แอตทริบิวต์นี้ใช้ในองค์ประกอบ AMP ได้ทุกองค์ประกอบ
โดยจะทำงานคล้ายกับคำค้นหาตามสื่อในสไตล์ชีตที่ใช้ทั้งเว็บไซต์
แต่มีผลเฉพาะกับองค์ประกอบที่เฉพาะเจาะจงในหน้าเว็บหน้าเดียว

ตัวอย่างเช่น เรามีรูปภาพ 2 ภาพที่มีคำค้นหาตามสื่อที่ใช้พร้อมกันไม่ได้

[sourcecode:html]
<amp-img
    media="(min-width: 650px)"
    src="wide.jpg"
    width=466
    height=355
    layout="responsive" >
</amp-img>
[/sourcecode]

จะมีการดึงภาพใดภาพหนึ่งขึ้นมาแสดงผล ขึ้นอยู่กับความกว้างของหน้าจอ

[sourcecode:html]
<amp-img
    media="(max-width: 649px)"
    src="narrow.jpg"
    width=527
    height=193
    layout="responsive" >
</amp-img>
[/sourcecode]

## การใช้ srcset และขนาด

ใช้แอตทริบิวต์ `srcset` เพื่อควบคุมเนื้อหาขององค์ประกอบ
โดยอิงจากนิพจน์ของสื่อที่หลากหลาย
กล่าวอย่างเจาะจงคือ ใช้แอตทริบิวต์นี้กับแท็ก [`amp-img`](/docs/reference/amp-img.html) ทั้งหมด
เพื่อระบุเนื้อหารูปภาพที่จะใช้โดยอิงตามขนาดหน้าจอที่หลากหลาย

ในตัวอย่างแบบง่ายนี้
`srcset` จะระบุภาพที่จะใช้โดยอิงตามความกว้างของหน้าจอ
ตัวบ่งชี้ `w` จะบอกความกว้างของ
ภาพแต่ละภาพในรายการแก่เบราว์เซอร์

[sourcecode:html]
<amp-img
    src="wide.jpg"
    srcset="wide.jpg" 640w,
           "narrow.jpg" 320w >
</amp-img>
[/sourcecode]

**หมายเหตุ:** AMP รองรับตัวบ่งชี้ `w` ในเบราว์เซอร์ทุกชนิด

เรียนรู้เพิ่มเติมเกี่ยวกับการสร้างรูปภาพที่ตอบสนองตามอุปกรณ์โดยใช้ `srcset`
ใน[การใช้รูปภาพที่ตอบสนองตามอุปกรณ์ (ตอนนี้เลย)](http://alistapart.com/article/using-responsive-images-now)

นอกจากนี้คุณยังสามารถใช้แอตทริบิวต์ `sizes` พร้อมไปกับ `srcset`
แอตทริบิวต์ `sizes` อธิบายวิธีคำนวณขนาดองค์ประกอบ
โดยอิงตามนิพจน์ใดๆ ก็ตามของสื่อ
โดย user agent จะเลือกซอร์สที่เกี่ยวข้องมากที่สุดที่แอตทริบิวต์ `srcset` ระบุไว้
โดยขึ้นอยู่กับขนาดที่คำนวณได้ขององค์ประกอบนั้น

ลองพิจารณาตัวอย่างต่อไปนี้

[sourcecode:html]
<amp-img
    src="wide.jpg"
    srcset="wide.jpg" 640w,
           "narrow.jpg" 320w
    sizes="(min-width: 650px) 50vw, 100vw" >
</amp-img>
[/sourcecode]

แอตทริบิวต์ `sizes` กำหนดความกว้างขององค์ประกอบเป็น 50% ของขนาดวิวพอร์ต เมื่อวิวพอร์ตมีขนาด 650 px ขึ้นไป
ตัวอย่างเช่น ถ้าวิวพอร์ตมีขนาด 800 px
ระบบจะกำหนดความกว้างขององค์ประกอบเป็น 400 px
จากนั้นเบราว์เซอร์จะเลือกทรัพยากร `srcset` ที่สัมพันธ์กับ 400 px
โดยสมมติว่าอัตราส่วนพิกเซลของอุปกรณ์คือ 1
ซึ่งในตัวอย่างนี้คือ `narrow.jpg` (320 px)

**สำคัญ:** เมื่อมีการระบุแอตทริบิวต์ขนาดร่วมกับความกว้างและความสูง
เค้าโครงจะมีค่าเริ่มต้นเป็น `responsive`

เรียนรู้เพิ่มเติมเกี่ยวกับการเปรียบเทียบแอตทริบิวต์ `sizes` และ `srcset`
กับคำค้นหาตามสื่อใน
บล็อกโพสต์ [Srcset และขนาด](https://ericportis.com/posts/2014/srcset-sizes/)

## รวมตัวยึดตำแหน่งและรายการสำรอง

### ตัวยึดตำแหน่ง

องค์ประกอบที่ทำเครื่องหมายว่าเป็นแอตทริบิวต์ `placeholder` ทำหน้าที่
เป็นตัวยึดตำแหน่งสำหรับองค์ประกอบ AMP ระดับบนสุด
ถ้าระบุไว้ องค์ประกอบ `placeholder` จะต้องเป็นองค์ประกอบระดับย่อยขององค์ประกอบ AMP นั้นโดยตรง

[sourcecode:html]
<amp-anim src="animated.gif" width=466 height=355 layout="responsive" >
    <amp-img placeholder src="preview.png" layout="fill"></amp-img>
</amp-anim>
[/sourcecode]

โดยค่าเริ่มต้น ระบบจะแสดงตัวยึดตำแหน่งสำหรับองค์ประกอบ AMP ทันที
แม้ว่าจะยังไม่มีการดาวน์โหลดหรือเริ่มต้นทรัพยากรขององค์ประกอบ AMP นั้น
แต่โดยปกติองค์ประกอบ AMP ดังกล่าวจะซ่อนตัวยึดตำแหน่งของมัน แล้วแสดงเนื้อหาเมื่อพร้อมแล้ว

**หมายเหตุ:** ตัวยึดตำแหน่งไม่จำเป็นต้องเป็นองค์ประกอบ AMP
องค์ประกอบ HTML ใดก็ตามทำหน้าที่เป็นตัวยึดตำแหน่งได้

### รายการสำรอง

ใช้แอตทริบิวต์ `fallback` เพื่อบ่งชี้พฤติกรรมในการใช้รายการสำรอง
สำหรับองค์ประกอบใดก็ตามที่เบราว์เซอร์ไม่รองรับ
ตัวอย่างเช่น ใช้แอตทริบิวต์ `fallback` เพื่อสื่อสารกับผู้ใช้
ว่าเบราว์เซอร์ไม่รองรับคุณลักษณะเฉพาะรายการใดรายการหนึ่ง

[sourcecode:html]
<amp-video width=400 height=300 src="https://yourhost.com/videos/myvideo.mp4"
    poster="myvideo-poster.jpg" >
  <div fallback>
        <p>Your browser doesn’t support HTML5 video.</p>
  </div>
</amp-video>
[/sourcecode]

แอตทริบิวต์ `fallback` สามารถตั้งค่าไว้ในองค์ประกอบ HTML ใดก็ได้ ไม่ใช่เพียงองค์ประกอบ AMP เท่านั้น
หากมีการระบุไว้ องค์ประกอบ `fallback` ต้องเป็นองค์ประกอบระดับย่อยขององค์ประกอบ AMP นั้นโดยตรง

### noloading

องค์ประกอบ AMP จำนวนมากได้รับอนุญาตพิเศษให้แสดง "ตัวบ่งชี้ว่ากำลังโหลด"
ซึ่งเป็นภาพเคลื่อนไหวแบบพื้นฐานที่แสดงให้เห็นว่าองค์ประกอบยังโหลดไม่สมบูรณ์
องค์ประกอบสามารถเลือกไม่ใช้พฤติกรรมนี้ได้โดยการเพิ่มแอตทริบิวต์ `noloading`
