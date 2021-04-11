---
title: Функции DWM
description: В этом разделе содержатся сведения о функциях диспетчер окон рабочего стола (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), функции
- DWM (диспетчер окон рабочего стола), функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339433"
---
# <a name="dwm-functions"></a>Функции DWM

В этом разделе содержатся сведения о функциях диспетчер окон рабочего стола (DWM).

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>двматтачмилконтент</strong></a><br/></td>
<td>Эта функция не реализована.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>двмдефвиндовпрок</strong></a><br/></td>
<td>Процедура окна по умолчанию для проверки попадания DWM в области, не являющейся клиентской.<br/> Также необходимо убедиться, что для <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> сообщения вызывается метод <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>двмдефвиндовпрок</strong></a> . Если <strong>двмдефвиндовпрок</strong> не вызывается для сообщения <strong>WM_NCMOUSELEAVE</strong> , DWM не удаляет выделение из кнопок <strong>развертывания</strong>, <strong>сворачивания</strong>и <strong>закрытия</strong> , когда курсор покидает окно.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>двмдетачмилконтент</strong></a><br/></td>
<td>Эта функция не реализована.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Включает эффект размытия для указанного окна.<br/></td>
<b>Примечание</b> . Начиная с Windows 8, вызов этой функции не приводит к эффекту размытия из-за изменения стиля в способе отрисовки окон.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>двменаблекомпоситион</strong></a><br/></td>
<td>Включает или отключает композицию DWM. <br/>
<blockquote>
[!Note]<br />
Эта функция является устаревшей по отношению к Windows 8. Диспетчер DWM больше не может быть отключен программным способом.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>двменаблеммксс</strong></a><br/></td>
<td>Уведомляет DWM о необходимости отказаться от планирования службы обработки отказов (MMCSS) класса мультимедиа, пока вызывающий процесс активен.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Расширяет рамку окна в клиентскую область.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>двмфлуш</strong></a><br/></td>
<td>Выдает вызов сброса, который блокирует вызывающий объект до следующего присутствия, когда все обновления Microsoft DirectX Surface, которые в настоящее время были выполнены. Это компенсирует очень сложный монтажный кадр или вызов процессов с очень низким приоритетом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>двмжетколоризатионколор</strong></a><br/></td>
<td>Извлекает текущий цвет, используемый для композиции DWM с эффектом стекла. Это значение основано на текущей цветовой схеме и может быть изменено пользователем. Приложения могут прослушивать изменения цвета, обрабатывая уведомление <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>двмжеткомпоситионтимингинфо</strong></a><br/></td>
<td>Извлекает сведения о текущем времени композиции для указанного окна.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>двмжетграфиксстреамклиент</strong></a><br/></td>
<td>Эта функция не реализована.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>двмжетграфиксстреамтрансформхинт</strong></a><br/></td>
<td>Эта функция не реализована.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>двмжеттранспортаттрибутес</strong></a><br/></td>
<td>Получает атрибуты транспорта.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>двмжетунметтабрекуирементс</strong></a><br/></td>
<td><blockquote>
<strong>Примечание</strong>  .  Эта функция является общедоступной, но нефункциональной для Windows 10, версии 1803.
</blockquote>
Проверяет требования, необходимые для получения вкладок в строке заголовка приложения для указанного окна.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>двмжетвиндоваттрибуте</strong></a><br/></td>
<td>Извлекает текущее значение указанного атрибута, примененного к окну.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>двминвалидатеиконикбитмапс</strong></a><br/></td>
<td>Вызывается приложением для указания того, что все ранее предоставленные точечные рисунки из окна, как эскизы, так и Просмотр представлений, должны быть обновлены.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Получает значение, указывающее, включена ли композиция DWM. Приложения на компьютерах под управлением Windows 7 или более ранней версии могут прослушивать изменения состояния композиции, обрабатывая уведомление <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>двммодифипревиаусдксфрамедуратион</strong></a><br/></td>
<td>Изменяет число обновлений монитора, с помощью которых будет отображаться предыдущий кадр. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Двммодифипревиаусдксфрамедуратион</strong></a> больше не поддерживается. Начиная с Windows 8.1, вызовы метода <strong>двммодифипревиаусдксфрамедуратион</strong> всегда возвращают E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>двмкуерисумбнаилсаурцесизе</strong></a><br/></td>
<td>Получает исходный размер эскиза DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Создает отношение эскиза DWM между конечным и исходным окнами.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>двмрендержестуре</strong></a><br/></td>
<td>Уведомляет DWM о том, что Контактное лицо было распознано как жест, и что DWM должен нарисовать отзыв для этого жеста.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>двмсетдксфрамедуратион</strong></a><br/></td>
<td>Задает число обновлений монитора, по которым отображается отображаемый кадр. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>Двмсетдксфрамедуратион</strong></a> больше не поддерживается. Начиная с Windows 8.1, вызовы метода <strong>двмсетдксфрамедуратион</strong> всегда возвращают E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>двмсетиконикливепревиевбитмап</strong></a><br/></td>
<td>Задает статический точечный рисунок для отображения <em>динамического предварительного просмотра</em> (также известного как <em>Предварительный просмотр</em>) окна или вкладки. Панель задач может использовать это растровое изображение, чтобы отобразить полный предварительный просмотр окна или вкладки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>двмсетикониксумбнаил</strong></a><br/></td>
<td>Задает статический точечный рисунок на окне или вкладке для использования в качестве эскиза. Панель задач может использовать это растровое изображение в качестве цели переключателя эскиза для окна или вкладки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>двмсетпресентпараметерс</strong></a><br/></td>
<td>Задает существующие параметры для компоновки кадра. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Двмсетпресентпараметерс</strong></a> больше не поддерживается. Начиная с Windows 8.1, вызовы метода <strong>двмсетпресентпараметерс</strong> всегда возвращают E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>двмсетвиндоваттрибуте</strong></a><br/></td>
<td>Задает значение для атрибутов окна, не являющихся клиентским рендерингом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>двмшовконтакт</strong></a><br/></td>
<td>Вызывается приложением или платформой для указания типа визуальной обратной связи для отображения в ответ на конкретный контакт или связь с пером.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>двмтесерконтакт</strong></a><br/></td>
<td>Позволяет выполнять графический отзыв о сенсорном взаимодействии и перетаскивать взаимодействия с пользователем.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>двмтранситионовнедвиндов</strong></a><br/></td>
<td>Координирует анимацию окон инструментов с помощью DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>двмунрегистерсумбнаил</strong></a><br/></td>
<td>Удаляет связь эскиза DWM, созданную функцией <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Обновляет свойства эскиза DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

