---
description: Следующие структуры объявляются в вспиксенгине. h.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структуры интерфейса захвата диагностики Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e1cefcf539996765b2e8055060277665f3cb9d31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537280"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Структуры интерфейса захвата диагностики Direct3D

Следующие структуры объявляются в вспиксенгине. h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>В этом разделе

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Раздел</th><th>Описание</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ресаурцепаир</strong></a></p></td><td><p>Представляет общий ресурс, который кодируется в виде строки COM.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>дескрипторхеапрекорд</strong></a></p></td><td><p>Представляет сведения о куче дескрипторов.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>пипелинестажееррор</strong></a></p></td><td><p>Представляет ошибку на этапе конвейера.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>пипелинестаже</strong></a></p></td><td><p>Представляет стадию конвейера, включая сведения об используемом шейдере.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>експерименттригжер</strong></a></p></td><td><p>Представляет сведения о триггере эксперимента.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>паккедкаллпкг</strong></a></p></td><td><p>Представляет пакет из четырех вызовов.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>симболсерверинфо</strong></a></p></td><td><p>Представляет сведения о сервере символов отладки.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>каллстаккфраме</strong></a></p></td><td><p>Представляет сведения о кадре в стеке вызовов.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>саурцефилеинфо</strong></a></p></td><td><p>Представляет сведения о файле исходного кода.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>суммаритем</strong></a></p></td><td><p>Представляет сводную информацию о событии.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>дебугшадер</strong></a></p></td><td><p>Представляет сведения о шейдере в отладчике.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Эксперимент</strong></a></p></td><td><p>Представляет сведения о эксперименте (захвате).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Проблема</strong></a></p></td><td><p>Представляет сведения о вопросе.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>Представляет двухмерную точку со целочисленными координатами без знака.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Представляет объемный индекс в данных потока</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>инпутлайаутструкт</strong></a></p></td><td><p>Представляет поля макета ввода для буфера вершин, по одному на поле в буфере вершин.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>пикселхисторйоператион</strong></a></p></td><td><p>Представляет сведения о журнале пикселей.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>пикселхисторинтерсектион</strong></a></p></td><td><p>Представляет сведения об определенном</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>мешдатабуфферлайаутентри</strong></a></p></td><td><p>Представляет сведения об отдельной записи в макете буфера сетки.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>дебугшадеррекуестинфо</strong></a></p></td><td><p>Представляет сведения о запросе отладчика шейдеров.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>Представляет вектор 4D с координатами целого числа со знаком.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>Представляет точку 4D с 64-битовыми координатами с плавающей запятой (Double).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>пиксенгинечаннелдеск</strong></a></p></td><td><p>Представляет описание канала цвета (образца).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>пиксенгинетекстуреформатдеск</strong></a></p></td><td><p>Представляет описание формата текстуры.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>пиксенгинетекстуредескриптор</strong></a></p></td><td><p>Представляет описание ресурса текстуры.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>пиксенгинетекстуреслицедескриптор</strong></a></p></td><td><p>Представляет описание среза текстуры.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>пиксенгинетекстуреслицеиндекс</strong></a></p></td><td><p>Представляет индекс среза текстуры</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>пиксенгинехистограм</strong></a></p></td><td><p>Представляет гистограмму текстуры.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Связанные темы

[Справочник по интерфейсу для захвата диагностики Direct3D](vspixengine-reference.md)

 

 
