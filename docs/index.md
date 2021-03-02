


## Audio samples

Below are the audio samples from step 300k, pinyin + hanzi + unet(as postnet). 

It may take some time to load all audios in browser. 

### Samples from training loop


<table>
   <thead>
      <tr>
         <th style="text-align: left">Synthesized</th>
         <th style="text-align: left">Groudtruth</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_0_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_0_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
      <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_1_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_1_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
     <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_2_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_2_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
      <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_3_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_3_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
      <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_4_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_4_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
      <tr>
         <td><audio controls="controls">
          <source src="./data/step_300000_5_postnet_waveglow.wav" autoplay="">
        </audio>
        </td>
         <td><audio controls="controls">
          <source src="./data/step_300000_5_ground-truth_waveglow.wav" autoplay="">
        </audio></td>
      </tr>
   </tbody>
</table>
  


### Novel synthsized samples

#### Input text
1. 黑化肥发灰会挥发,灰化肥挥发会发黑
2. 红鲤鱼绿鲤鱼与驴
3. 前方路口左转，然后在下一个路口右转
4. 请输入您的卡号.您输入的卡号是六二二六,三八七六,零三四七,六九一五
5. 天青色等烟雨,而我在等你,炊烟袅袅升起，隔江千万里
6. 我听不清你在说什么，请大声一点
7. 如果觉得这个项目好，请手动加个星吧，感谢
8. 小毛豆你好，很高兴认识你.寒假马上要结束了.我觉得你最近有进步，继续加油.晚上要早点睡觉,因为明天要开学了.
9. 有个小孩叫小杜,上街打醋又买布.买了布打了醋,回头看见鹰抓兔.放下布搁下醋,上前去追鹰和兔.飞了鹰跑了兔,洒了醋湿了布.


#### Audio samples

To generate audio samples, first you need to down load the checkpoint from <a href="https://drive.google.com/file/d/11mBus5gn69_KwvNec9Zy9jjTs3LgHdx3/view?usp=sharing">google drive</a> an untar it to mandarin_tts/


Then the audio samples are genreated by the following command:
``` 
./scripts/hz_synth.sh 1.0 300000
./scripts/hz_synth.sh 0.9 300000 
./scripts/hz_synth.sh 1.1 300000 
```

You can also use pure pinyin + unet model, as follows:
``` 
./scripts/py_synth.sh 1.0 300000 
./scripts/py_synth.sh 0.9 300000 
./scripts/py_synth.sh 1.1 300000 
```


For other text inputs, you can alter text in input.txt. Some hints: 
- 只需输入中文，因为代码中使用了pypinyin进行转换，转换前先分词。 
- 不同句子用句号分开，可放在同一行，最后同一行的句子会合并成一个语音。如果需要不同语音，放在不同行即可。
- 需要停顿的地方用逗号。
- 算法不区分问号和叹号，当成句号处理。同样，不区分顿号，当成逗号，token统一设置为sp1. 


<table>
   <thead>
      <tr>
         <th style="text-align: left">Text</th>
         <th style="text-align: left">Normal</th>
         <th style="text-align: left">Fast</th>
         <th style="text-align: left">slow</th>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td>1
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_黑化肥发灰会挥发,灰化肥挥发会发黑.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_黑化肥发灰会挥发,灰化肥挥发会发黑.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_黑化肥发灰会挥发,灰化肥挥发会发黑.wav" autoplay="">
        </audio></td>
      </tr>
          <tr>
         <td>2
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_红鲤鱼绿鲤鱼与驴.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_红鲤鱼绿鲤鱼与驴.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_红鲤鱼绿鲤鱼与驴.wav" autoplay="">
        </audio></td>
      </tr>
        <tr>
         <td>3
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_前方路口左转，然后在下一个路口右转.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_前方路口左转，然后在下一个路口右转.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_前方路口左转，然后在下一个路口右转.wav" autoplay="">
        </audio></td>
      </tr>
         <tr>
         <td>4
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_请输入您的卡号.您输入的卡号是六二二六,三八七六,零三四七,六九.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_请输入您的卡号.您输入的卡号是六二二六,三八七六,零三四七,六九.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_请输入您的卡号.您输入的卡号是六二二六,三八七六,零三四七,六九.wav" autoplay="">
        </audio></td>
      </tr>
         <tr>
         <td>5
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_天青色等烟雨,而我在等你,炊烟袅袅升起，隔江千万里.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_天青色等烟雨,而我在等你,炊烟袅袅升起，隔江千万里.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_天青色等烟雨,而我在等你,炊烟袅袅升起，隔江千万里.wav" autoplay="">
        </audio></td>
      </tr>
         <tr>
         <td>6
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_我听不清你在说什么，请大声一点.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_我听不清你在说什么，请大声一点.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_我听不清你在说什么，请大声一点.wav" autoplay="">
        </audio></td>
      </tr>
         <tr>
         <td>7
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_如果觉得这个项目好，请手动加个星吧，感谢.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_如果觉得这个项目好，请手动加个星吧，感谢.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_如果觉得这个项目好，请手动加个星吧，感谢.wav" autoplay="">
        </audio></td>
      </tr>
       <tr>
         <td>8
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_小毛豆你好，很高兴认识你.寒假马上要结束了.我觉得你最近有进步，.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_小毛豆你好，很高兴认识你.寒假马上要结束了.我觉得你最近有进步，.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_小毛豆你好，很高兴认识你.寒假马上要结束了.我觉得你最近有进步，.wav" autoplay="">
        </audio></td>
      </tr>
    <tr>
      <td>9
        </td>
         <td><audio controls="controls">
          <source src="./novel/hz_1.0_300000_有个小孩叫小杜,上街打醋又买布.买了布打了醋,回头看见鹰抓兔.放.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_0.9_300000_有个小孩叫小杜,上街打醋又买布.买了布打了醋,回头看见鹰抓兔.放.wav" autoplay="">
        </audio></td>
          <td><audio controls="controls">
          <source src="./novel/hz_1.1_300000_有个小孩叫小杜,上街打醋又买布.买了布打了醋,回头看见鹰抓兔.放.wav" autoplay="">
        </audio></td>
      </tr>
      
      
   </tbody>
</table>
  