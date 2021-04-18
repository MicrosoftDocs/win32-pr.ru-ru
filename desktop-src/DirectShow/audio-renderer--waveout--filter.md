---
description: Фильтр модуля подготовки звука (звук)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Фильтр модуля подготовки звука (звук)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f47018d22bcbbdcf884f5eb4356d1d0b3fe60d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682312"
---
# <a name="audio-renderer-waveout-filter"></a>Фильтр модуля подготовки звука (звук)

Этот фильтр использует \* API-интерфейс для вывода звуковых сигналов. Однако [Фильтр рендеринга DirectSound](directsound-renderer-filter.md) предоставляет те же функциональные возможности, что и DirectSound. По умолчанию диспетчер графов фильтров использует модуль подготовки DirectSound вместо этого фильтра. Микширование звука отключено в модуле подготовки аудио, поэтому если во время воспроизведения необходимо смешивать несколько звуковых потоков, используйте модуль подготовки DirectSound.

Этот фильтр не проверяет подтип аудиопотока. Структура [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat) или [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , переданная в формате, содержит сведения, необходимые для соединения.

Этот фильтр поддерживает ряд частот выборки, которые зависят от звукового драйвера.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Интерфейсы фильтра</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>иамаудиорендерерстатс</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>иамклоккславе</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>иамдиректсаунд</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>иамресаурцеконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ибасефилтер</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>ибасикаудио</strong></a></li>
<li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>имедиапоситион</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>имедиасикинг</strong></a></li>
<li>IPersistPropertyBag</li>
<li>IPersistStream</li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>иреференцеклокк</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Типы носителей входных закрепления</td>
<td><strong>MEDIATYPE_Audio</strong></td>
</tr>
<tr class="odd">
<td>Интерфейсы входных закрепления</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>имеминпутпин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>ипин</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>Типы носителей для выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="odd">
<td>Интерфейсы выходного ПИН-кода</td>
<td>Не применяется</td>
</tr>
<tr class="even">
<td>Фильтровать CLSID</td>
<td><strong>CLSID_AudioRender</strong></td>
</tr>
<tr class="odd">
<td>CLSID страницы свойств</td>
<td><strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong></td>
</tr>
<tr class="even">
<td>Исполняемый объект</td>
<td>quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Заслуживают</a></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Категория фильтра</a></td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 
