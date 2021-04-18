---
description: '\_Константы DXGI Present указывают параметры для представления кадров в выходных данных.'
ms.assetid: 1ddf8643-ea3e-4c9f-8439-c245942f7333
title: DXGI_PRESENT (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a21d53159572a52b372774e4988e775744ede5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703752"
---
# <a name="dxgi_present"></a>\_присутствующая DXGI

Константы **DXGI \_ Present** указывают параметры для представления кадров в выходных данных.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span></span><dl> <dt><strong></strong></dt>значение <dt>0</dt> </dl></td>
<td style="text-align: left;">Представление кадра из каждого буфера (начиная с текущего буфера) с выходом.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_SEQUENCE"></span><span id="dxgi_present_do_not_sequence"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_SEQUENCE</strong></dt> <dt>0x00000002UL</dt> </dl></td>
<td style="text-align: left;">Представьте кадр из текущего буфера в выходные данные. Используйте этот флаг, чтобы презентация могла использовать по вертикали, а не последовательные буферы в цепочке обычным способом.<br/>
<blockquote>
[!Note]<br />
Если вызывающее приложение задает DXGI_PRESENT_DO_NOT_SEQUENCE константу в первой текущей операции (то есть, если нет текущего буфера), среда выполнения игнорирует эту операцию и не вызывает драйвер.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_TEST"></span><span id="dxgi_present_test"></span><dl> <dt><strong>DXGI_PRESENT_TEST</strong></dt> <dt>0x00000001UL</dt> </dl></td>
<td style="text-align: left;">Не показывать кадр в выходных данных. Будет протестировано состояние цепочки буферов, и будут возвращены соответствующие ошибки. DXGI_PRESENT_TEST предназначено для использования только при переключении из состояния простоя; не используйте его, чтобы определить, когда следует переключиться на состояние простоя, так как это может привести к выходу цепочки буферов, что не сможет выйти из полноэкранного режима.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTART"></span><span id="dxgi_present_restart"></span><dl> <dt><strong>DXGI_PRESENT_RESTART</strong></dt> <dt>0x00000004UL</dt> </dl></td>
<td style="text-align: left;">Указывает, что среда выполнения отклоняет незавершенные постановки в очередь.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_DO_NOT_WAIT"></span><span id="dxgi_present_do_not_wait"></span><dl> <dt><strong>DXGI_PRESENT_DO_NOT_WAIT</strong></dt> <dt>0x00000008UL</dt> </dl></td>
<td style="text-align: left;">Указывает, что среда выполнения не сможет выполнить презентацию (то есть вызвать сбой вызова <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>IDXGISwapChain1::P resent1</strong></a>) с кодом ошибки <a href="dxgi-error.md">DXGI_ERROR_WAS_STILL_DRAWING</a> , если вызывающий поток заблокирован. среда выполнения возвращает DXGI_ERROR_WAS_STILL_DRAWING, а не спящий режим, пока не будет разрешена зависимость.<br/> <strong>Direct3D 11:</strong> Это значение перечисления поддерживается начиная с Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_RESTRICT_TO_OUTPUT"></span><span id="dxgi_present_restrict_to_output"></span><dl> <dt><strong>DXGI_PRESENT_RESTRICT_TO_OUTPUT</strong></dt> <dt>0x00000010UL</dt> </dl></td>
<td style="text-align: left;">Указывает, что содержимое презентации будет отображаться только для определенных выходных данных. Содержимое не будет отображаться в других выходных данных. Например, если пользователь пытается перенести содержимое видео на другой выход, содержимое видео не будет отображаться. <br/> <strong>Direct3D 11:</strong> Это значение перечисления поддерживается начиная с Windows 8. <br/>
<blockquote>
[!Note]<br />
Этот флаг следует использовать только с действием Swap <a href="/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> или DXGI_SWAP_EFFECT_FLIP_DISCARD. Использование этого флага с <em>другими</em> эффектами перекачки является устаревшим и может не работать в будущих версиях Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_PREFER_RIGHT"></span><span id="dxgi_present_stereo_prefer_right"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_PREFER_RIGHT</strong></dt> <dt>0x00000020UL</dt> </dl></td>
<td style="text-align: left;">Указывает, что если стереосистема должна быть уменьшена до Mono, используется просмотр с правильным глазом, а не видимый режим просмотра слева.<br/> <strong>Direct3D 11:</strong> Это значение перечисления поддерживается начиная с Windows 8.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_STEREO_TEMPORARY_MONO"></span><span id="dxgi_present_stereo_temporary_mono"></span><dl> <dt><strong>DXGI_PRESENT_STEREO_TEMPORARY_MONO</strong></dt> <dt>0x00000040UL</dt> </dl></td>
<td style="text-align: left;">Указывает, что в презентации должен использоваться левый буфер в качестве буфера Mono. Приложение вызывает метод <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported"><strong>IDXGISwapChain1:: истемпораримоносуппортед</strong></a> , чтобы определить, поддерживает ли цепочка обмена &quot; временный Mono &quot; .<br/> <strong>Direct3D 11:</strong> Это значение перечисления поддерживается начиная с Windows 8.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="DXGI_PRESENT_USE_DURATION"></span><span id="dxgi_present_use_duration"></span><dl> <dt><strong>DXGI_PRESENT_USE_DURATION</strong></dt> <dt>0x00000100UL</dt> </dl></td>
<td style="text-align: left;">Этот флаг должен быть установлен в приложениях мультимедиа, которые в настоящее время используют настраиваемый длительный период (настраиваемая частота обновления). См. <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia"><strong>идксгисвапчаинмедиа</strong></a>.<br/>
<blockquote>
[!Note]<br />
Это значение поддерживается начиная с Windows 8.1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="DXGI_PRESENT_ALLOW_TEARING"></span><span id="dxgi_present_allow_tearing"></span><dl> <dt><strong>DXGI_PRESENT_ALLOW_TEARING</strong></dt> <dt>0x00000200UL</dt> </dl></td>
<td style="text-align: left;">Разрешение на разрывы является обязательным для отображения частоты обновления переменных.<br/> Условия использования DXGI_PRESENT_ALLOW_TEARING в настоящее время приведены ниже.<br/>
<ul>
<li>Цепь подкачки должна быть создана с флагом <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag"><strong>DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</strong></a> .</li>
<li>Интервал синхронизации, переданный в значение <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (или <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>), должен быть равен 0.</li>
<li>Флаг DXGI_PRESENT_ALLOW_TEARING не может использоваться в приложении, которое в настоящее время находится в режиме монопольного доступа на весь экран (устанавливается путем вызова <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate"><strong>сетфуллскринстате (true)</strong></a>). Его можно использовать только в оконном режиме. Чтобы использовать этот флаг в полноэкранных приложениях Win32, приложение должно быть представлено в полноэкранном режиме без рамки и отключить автоматическое переключение ALT + ВВОД в полноэкранном режиме с помощью <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation"><strong>идксгифактори:: макевиндовассоЦиатион</strong></a>. Приложения UWP, выполняющие переход в полноэкранный режим путем вызова <code>Windows::UI::ViewManagement::ApplicationView::TryEnterFullscreen()</code> , — это окна без рамки, которые могут использовать флаг.</li>
</ul>
Вызов <a href="/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present"><strong>Present</strong></a> (или <a href="/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1"><strong>Present1</strong></a>) с этим флагом и не удовлетворяет указанным выше условиям приведет к возвращению DXGI_ERROR_INVALID_CALL ошибки в вызывающее приложение.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Параметры представления предоставляются во время вызова [**идксгисвапчаин::P**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) повторной отправки или [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Буферы указываются в описании цепочки буфера обмена (см. раздел [**\_ \_ \_ цепочки подкачки DXGI**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) или [**\_ \_ цепочка \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)).

Перезагрузка DXGI \_ Present \_ допустима только для цепочек перелистывания моделей и во весь экран. Приложения могут использовать \_ \_ перезагрузку DXGI, чтобы восстанавливаться после сбоев при воспроизведении, а также удалять ранее поставленные в очередь презентации. Отмена ранее поставленных в очередь презентаций полезна, если эти презентации в очереди являются оконными сценариями. В частности, ранее поставленная в очередь презентация могла предположить, что окно имеет старый размер (то есть операция изменения размера была выполнена после отправки).

\_Поток DXGI Present \_ restrict \_ \_ является допустимым только для цепочек переключения, которые задают определенные выходные данные, чтобы ограничить содержимое до создания этих цепочек подкачки ([**IDXGIFactory2:: креатесвапчаинфорхвнд**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)). Если нет выходных данных для ограничения, флаг является недопустимым.

\_Режим DXGI \_ , \_ Предпочитаемый стерео \_ , указывает, что если стерео должен быть уменьшен до Mono, следует использовать правильный глаз, а не левый глаз (по умолчанию). Этот флаг можно использовать, если одна сторона имеет более высокий уровень качества (например, если пара стерео является синтезированной на стандартном образе).

\_Наличие \_ стерео временного стереофонический объект DXGI указывает на то \_ \_ , что текущий должен использовать левый буфер в качестве буфера Mono. Этот флаг можно использовать, чтобы избежать обновления правильного буфера, когда приложение временно не имеет стерео содержимого. Этот флаг следует использовать, когда это возможно, так как он обеспечивает значительную оптимизацию операционной системой и в некоторых обстоятельствах может избежать видимых артефактов изменения режима.

Для \_ \_ \_ \_ переключения на цепочку Mono для большинства приложений, которые предполагается использовать стереосистему, следует использовать флаг "DXGI Present стерео Temporary моно" в настройках. Необходимо сбалансировать использование этого флага в приложениях, которые выполняются очень долго или редко отображают стерео для недостатка неиспользуемой памяти.

> [!Note]  
> Полноэкранные приложения, переключились на цепочку буфера обмена, вызывают изменение режима, которое обычно имеет видимые артефакты (например, "мигает"). Однако временный моно может не поддерживаться для цепочек переключения в полноэкранный режим.

 

В \_ презентации DXGI Present \_ стерео \_ ПРЕДПОЧИТАТЬ \_ право и DXGI \_ Present \_ \_ временные \_ Флаги моно применяются только к цепочкам стерео swap. Если вы используете их при наличии цепочек подкачки, выполняется Недопустимая операция.

Если при \_ \_ \_ \_ наличии цепочки стереозвука, которая не поддерживает временный моно, используется флаг "DXGI Present стерео", то возникает ошибка, цепочка буферов не отображается, и презентация возвращает [ \_ ошибку \_ Недопустимый \_ вызов](dxgi-error.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 
