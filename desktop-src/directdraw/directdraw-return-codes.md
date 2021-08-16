---
title: Коды возврата DirectDraw (Ддрав. h)
description: Коды возврата DirectDraw — ошибки представлены отрицательными значениями и не могут быть объединены.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e937ad9cc32a7837303d535b73b176c7e16f2d0ab0033bf625f629d2d5f7bc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504356"
---
# <a name="directdraw-return-codes"></a>Коды возврата DirectDraw

Ошибки представлены отрицательными значениями и не могут быть объединены. В этой таблице перечислены значения, которые могут быть возвращены всеми методами [интерфейсов DirectDraw](directdraw-interfaces.md) и [функций DirectDraw](directdraw-functions.md). Список кодов ошибок, которые может возвращать каждый метод или функция, см. в описании метода или функции.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**ДД \_ ОК**
</dt> <dd> <dl> <dt>



Запрос успешно выполнен.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**ДДЕРР \_ алреадинитиализед**
</dt> <dd> <dl> <dt>



Объект уже инициализирован.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**ДДЕРР \_ блтфасткантклип**
</dt> <dd> <dl> <dt>



Объект Директдравклиппер присоединяется к исходной поверхности, которая была передана в вызов метода [**IDirectDrawSurface7:: блтфаст**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**ДДЕРР \_ каннотаттачсурфаце**
</dt> <dd> <dl> <dt>



Поверхность не может быть присоединена к другой запрошенной поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**ДДЕРР \_ каннотдетачсурфаце**
</dt> <dd> <dl> <dt>



Поверхность не может быть отсоединена от другой запрошенной поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**ДДЕРР \_ канткреатедк**
</dt> <dd> <dl> <dt>



Windows не может создать дополнительные контексты устройств (DCs), или контроллер домена запросил область с индексированной палитрой, когда у поверхности не было палитры и режим отображения не индексирован (в данном случае DirectDraw не может выбрать правильную палитру в контроллере домена).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**ДДЕРР \_ кантдупликате**
</dt> <dd> <dl> <dt>



Основные и трехмерные поверхности или поверхности, созданные неявно, не могут дублироваться.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**ДДЕРР \_ кантлокксурфаце**
</dt> <dd> <dl> <dt>



Доступ к этой поверхности отклонен, так как была предпринята попытка заблокировать основную поверхность без поддержки интерфейса управления отображением (ДЦИ).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**ДДЕРР \_ кантпажелокк**
</dt> <dd> <dl> <dt>



Сбой попытки блокировки страницы в области. Блокировка страницы не работает на поверхности отображения памяти или на эмуляторе основной поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**ДДЕРР \_ кантпажеунлокк**
</dt> <dd> <dl> <dt>



Ошибка при разблокировании поверхности на странице. Разблокировка страниц не работает на поверхности отображения памяти или на эмуляторе основной поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**ДДЕРР \_ клипперисусингхвнд**
</dt> <dd> <dl> <dt>



Предпринята попытка задать список клипов для объекта Директдравклиппер, который уже отслеживает обработчик окна.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**ДДЕРР \_ колоркэйнотсет**
</dt> <dd> <dl> <dt>



Для этой операции не указан ключ цвета источника.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**ДДЕРР \_ куррентлинотаваил**
</dt> <dd> <dl> <dt>



В настоящее время поддержка недоступна.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**ДДЕРР \_ ддскапскомплексрекуиред**
</dt> <dd> <dl> <dt>



Новое для DirectX 7,0. Для поверхности требуется \_ сложный флаг ддскапс.


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**ДДЕРР \_ дкалреадикреатед**
</dt> <dd> <dl> <dt>



Для этой поверхности уже возвращен контекст устройства (DC). Для каждой поверхности можно получить только один контроллер домена.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>ДДЕРР \_ девицедоеснтовнсурфаце**
</dt> <dd> <dl> <dt>



Поверхности, созданные одним устройством DirectDraw, не могут напрямую использоваться другим устройством DirectDraw.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>ДДЕРР \_ директдравалреадикреатед**
</dt> <dd> <dl> <dt>



Объект DirectDraw, представляющий этот драйвер, уже создан для этого процесса.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_исключение ддерр**
</dt> <dd> <dl> <dt>



При выполнении запрошенной операции было обнаружено исключение.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**ДДЕРР \_ ексклусивемодеалреадисет**
</dt> <dd> <dl> <dt>



Предпринята попытка установить совместный уровень, если он уже был установлен в монопольном режиме.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**\_срок действия ддерр истек**
</dt> <dd> <dl> <dt>



Срок действия данных истек, поэтому они больше не действительны.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**ДДЕРР \_ Generic**
</dt> <dd> <dl> <dt>



Неопределенное условие ошибки.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**ДДЕРР \_ хеигхталигн**
</dt> <dd> <dl> <dt>



Высота указанного прямоугольника не кратна требуемому выравниванию.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**ДДЕРР \_ хвндалреадисет**
</dt> <dd> <dl> <dt>



Обработчик окна с поддержкой DirectDraw-уровня уже задан. Он не может быть сброшен, пока для процесса созданы поверхности или палитры.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**ДДЕРР \_ хвндсубклассед**
</dt> <dd> <dl> <dt>



DirectDraw не может восстановить состояние из-за того, что многоуровневый оконный обработчик DirectDraw является подклассом.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**ДДЕРР \_ имплиЦитликреатед**
</dt> <dd> <dl> <dt>



Невозможно восстановить поверхность, так как она является неявно созданной поверхностью.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**ДДЕРР \_ инкомпатиблепримари**
</dt> <dd> <dl> <dt>



Запрос на создание основной поверхности не соответствует существующей первичной поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**ДДЕРР \_ инвалидкапс**
</dt> <dd> <dl> <dt>



Одна или несколько битов возможностей, переданных функции обратного вызова, неверны.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**ДДЕРР \_ инвалидклиплист**
</dt> <dd> <dl> <dt>



DirectDraw не поддерживает указанный список клипов.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**ДДЕРР \_ инвалиддиректдравгуид**
</dt> <dd> <dl> <dt>



Глобальный уникальный идентификатор (GUID), переданный функции [**директдравкреате**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) , не является допустимым идентификатором драйвера DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**ДДЕРР \_ инвалидмоде**
</dt> <dd> <dl> <dt>



DirectDraw не поддерживает запрошенный режим.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**ДДЕРР \_ инвалидобжект**
</dt> <dd> <dl> <dt>



DirectDraw получил указатель, который являлся недопустимым объектом DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**ДДЕРР \_ инвалидпарамс**
</dt> <dd> <dl> <dt>



Один или несколько параметров, переданных в метод, неверны.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**ДДЕРР \_ инвалидпикселформат**
</dt> <dd> <dl> <dt>



Формат пикселей был недопустимым, как указано.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**ДДЕРР \_ инвалидпоситион**
</dt> <dd> <dl> <dt>



Расположение оверлея в месте назначения больше не является допустимым.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**ДДЕРР \_ инвалидрект**
</dt> <dd> <dl> <dt>



Указан недопустимый прямоугольник.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**ДДЕРР \_ инвалидстреам**
</dt> <dd> <dl> <dt>



Указанный поток содержит недопустимые данные.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**ДДЕРР \_ инвалидсурфацетипе**
</dt> <dd> <dl> <dt>



Неверный тип поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**ДДЕРР \_ локкедсурфацес**
</dt> <dd> <dl> <dt>



Одна или несколько поверхностей заблокированы, что приводит к сбою запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**ДДЕРР \_ MOREDATA**
</dt> <dd> <dl> <dt>



Доступно больше данных, чем может вместить указанный размер буфера.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**ДДЕРР \_ использованием NewMode**
</dt> <dd> <dl> <dt>



Новое для DirectX 7,0. Когда [**IDirectDraw7:: стартмодетест**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) вызывается с \_ флагом ддсмт истестрекуиред, он может вернуть это значение, чтобы отметить, что некоторые или все разрешения можно и следует протестировать. [**IDirectDraw7:: евалуатемоде**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) возвращает это значение, указывающее, что тест переключен на новый режим отображения.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**ДДЕРР \_ NO3D**
</dt> <dd> <dl> <dt>



Отсутствует трехмерное оборудование или эмуляция.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**ДДЕРР \_ ноалфахв**
</dt> <dd> <dl> <dt>



Оборудование с альфа-ускорением отсутствует или доступно, что приводит к сбою запрошенной операции.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**ДДЕРР \_ ноблсв**
</dt> <dd> <dl> <dt>



Нет битового блока, поступающего в передачу.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**ДДЕРР \_ ноклиплист**
</dt> <dd> <dl> <dt>



Список клипов недоступен.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**ДДЕРР \_ ноклипператтачед**
</dt> <dd> <dl> <dt>



К объекту Surface не присоединен объект Директдравклиппер.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**ДДЕРР \_ ноколорконвхв**
</dt> <dd> <dl> <dt>



Оборудование для преобразования цветов отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**ДДЕРР \_ ноколоркэй**
</dt> <dd> <dl> <dt>



У поверхности пока нет ключа цвета.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**ДДЕРР \_ ноколоркэйхв**
</dt> <dd> <dl> <dt>



Отсутствует поддержка оборудования для ключа цвета назначения.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**ДДЕРР \_ нокуперативелевелсет**
</dt> <dd> <dl> <dt>



Функция Create была вызвана без метода [**IDirectDraw7:: сеткуперативелевел**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**ДДЕРР \_ нодк**
</dt> <dd> <dl> <dt>



Для этой поверхности не был создан контекст устройства (DC).


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**ДДЕРР \_ ноддропшв**
</dt> <dd> <dl> <dt>



Оборудование DirectDraw-Operation (верхнем) не доступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**ДДЕРР \_ нодиректдравхв**
</dt> <dd> <dl> <dt>



Создание объекта DirectDraw с аппаратным обеспечением невозможно; драйвер не поддерживает оборудование.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**ДДЕРР \_ нодиректдравсуппорт**
</dt> <dd> <dl> <dt>



Поддержка DirectDraw с текущим драйвером экрана невозможна.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**ДДЕРР \_ нодриверсуппорт**
</dt> <dd> <dl> <dt>



Новое для DirectX 7,0. Продолжение тестирования невозможно, так как драйвер видеоадаптера не перечисляет частоты обновления.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**\_Эмуляция ддерр**
</dt> <dd> <dl> <dt>



Эмуляция программного обеспечения недоступна.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**ДДЕРР \_ ноексклусивемоде**
</dt> <dd> <dl> <dt>



Для операции требуется, чтобы приложение имело монопольный режим, но приложение не имеет монопольного режима.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**ДДЕРР \_ нофлифв**
</dt> <dd> <dl> <dt>



Зеркальное отображение видимых поверхностей не поддерживается.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**ДДЕРР \_ нофокусвиндов**
</dt> <dd> <dl> <dt>



Предпринята попытка создать или задать окно устройства без предварительного задания фокусного окна.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**ДДЕРР \_ ногди**
</dt> <dd> <dl> <dt>



GDI отсутствует.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**ДДЕРР \_ HWND**
</dt> <dd> <dl> <dt>



для Clipper уведомления требуется обработчик окна, или в качестве обработчика окна параллельного уровня не был ранее установлен маркер окна.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**ДДЕРР \_ номипмафв**
</dt> <dd> <dl> <dt>



Оборудование для сопоставления текстур, поддерживающее mipmap, отсутствует или доступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**ДДЕРР \_ номиррорхв**
</dt> <dd> <dl> <dt>



Оборудование зеркального отображения отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**ДДЕРР \_ номониторинформатион**
</dt> <dd> <dl> <dt>



Новое для DirectX 7,0. Продолжение тестирования невозможно, так как монитор не имеет связанных данных EDID.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**ДДЕРР \_ нононлокалвидмем**
</dt> <dd> <dl> <dt>



Предпринята попытка выделить нелокальную видеопамять на устройстве, которое не поддерживает нелокальную видеопамять.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**ДДЕРР \_ нуптимизехв**
</dt> <dd> <dl> <dt>



Устройство не поддерживает оптимизированные поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**ДДЕРР \_ нуверлайдест**
</dt> <dd> <dl> <dt>



Метод [**IDirectDrawSurface7:: жетоверлайпоситион**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) вызывается для оверлея, который метод [**IDirectDrawSurface7:: упдатеоверлай**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) не вызывал для установки в качестве назначения.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**ДДЕРР \_ нуверлайхв**
</dt> <dd> <dl> <dt>



Оборудование оверлея отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**ДДЕРР \_ нопалеттеаттачед**
</dt> <dd> <dl> <dt>



К этой поверхности не присоединен объект палитры.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**ДДЕРР \_ нопалеттехв**
</dt> <dd> <dl> <dt>



Отсутствует аппаратная поддержка 16-или 256-цветовых палитр.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**ДДЕРР \_ норастерофв**
</dt> <dd> <dl> <dt>



Соответствующее оборудование точечной операции отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**ДДЕРР \_ норотатионхв**
</dt> <dd> <dl> <dt>



Оборудование для вращения отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**ДДЕРР \_ ностереохардваре**
</dt> <dd> <dl> <dt>



Стерео оборудование отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**ДДЕРР \_ ностретчхв**
</dt> <dd> <dl> <dt>



Аппаратная поддержка для растяжения отсутствует.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**ДДЕРР \_ носурфацелефт**
</dt> <dd> <dl> <dt>



Отсутствует оборудование, поддерживающее стерео поверхности.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**ДДЕРР \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



Объект Директдравсурфаце не использует 4-разрядную цветовую палитру, и для выполнения запрошенной операции требуется 4-разрядная цветовая палитра.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**ДДЕРР \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



Объект Директдравсурфаце не использует 4-разрядную палитру индекса цвета, и для запрошенной операции требуется 4-разрядная палитра индекса цвета.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**ДДЕРР \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



Объект Директдравсурфаце не использует 8-разрядную цветовую палитру, и для выполнения запрошенной операции требуется 8-разрядная цветовая палитра.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**ДДЕРР \_ нотаоверлайсурфаце**
</dt> <dd> <dl> <dt>



Для неналоженной поверхности вызывается компонент оверлея.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**ДДЕРР \_ нотекстурехв**
</dt> <dd> <dl> <dt>



Операция не может быть выполнена, так как оборудование для сопоставления текстур отсутствует или недоступно.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**ДДЕРР \_ нотфлиппабле**
</dt> <dd> <dl> <dt>



Предпринята попытка перевернуть поверхность, которая не может быть отражена.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**ДДЕРР \_ NotFound**
</dt> <dd> <dl> <dt>



Запрашиваемый элемент не найден.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**ДДЕРР \_ нотинитиализед**
</dt> <dd> <dl> <dt>



Была предпринята попытка вызвать метод интерфейса объекта DirectDraw, созданного функцией [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) до инициализации объекта.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**ДДЕРР \_ загружен»**
</dt> <dd> <dl> <dt>



Поверхность — это оптимизированная поверхность, но она пока не выделила память.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**ДДЕРР \_ нотлоккед**
</dt> <dd> <dl> <dt>



Предпринята попытка разблокировать незаблокированную поверхность.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**ДДЕРР \_ нотпажелоккед**
</dt> <dd> <dl> <dt>



Была предпринята попытка разблокировки поверхности без необработанных блокировок страниц.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**ДДЕРР \_ нотпалеттизед**
</dt> <dd> <dl> <dt>



Используемая поверхность не является поверхностью на основе палитры.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**ДДЕРР \_ новсинчв**
</dt> <dd> <dl> <dt>



Аппаратная поддержка вертикальных пустых синхронизированных операций не поддерживается.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**ДДЕРР \_ нозбуфферхв**
</dt> <dd> <dl> <dt>



Операция создания z-буфера в отображаемой памяти или выполнения блочного блока (BitBlt) с помощью z-буфера не может быть выполнена, так как отсутствует поддержка аппаратных буферов z.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**ДДЕРР \_ нозоверлайхв**
</dt> <dd> <dl> <dt>



Поверхности наложения не могут быть z-слоями на основе z-порядка, так как оборудование не поддерживает z-порядок наложений.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**ДДЕРР \_ аутофкапс**
</dt> <dd> <dl> <dt>



Оборудование, необходимое для запрошенной операции, уже выделено.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**ДДЕРР \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>



DirectDraw не хватает памяти для выполнения операции.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**ДДЕРР \_ аутофвидеомемори**
</dt> <dd> <dl> <dt>



DirectDraw не имеет достаточно памяти для выполнения операции.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**ДДЕРР \_ оверлаппингректс**
</dt> <dd> <dl> <dt>



Исходный и конечный прямоугольники находятся на одной поверхности и перекрываются друг с другом.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**ДДЕРР \_ оверлайкантклип**
</dt> <dd> <dl> <dt>



Оборудование не поддерживает обрезанные наложения.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**ДДЕРР \_ оверлайколоркэйонлйонеактиве**
</dt> <dd> <dl> <dt>



Предпринята попытка активировать более одного цвета ключа на наложении.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**ДДЕРР \_ оверлайнотвисибле**
</dt> <dd> <dl> <dt>



Метод [**IDirectDrawSurface7:: жетоверлайпоситион**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) был вызван для скрытого оверлея.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**ДДЕРР \_ палеттебуси**
</dt> <dd> <dl> <dt>



Доступ к этой палитре отклонен, так как палитра заблокирована другим потоком.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**ДДЕРР \_ примарисурфацеалреадексистс**
</dt> <dd> <dl> <dt>



Этот процесс уже создал основную поверхность.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**ДДЕРР \_ регионтусмалл**
</dt> <dd> <dl> <dt>



Регион, переданный методу [**идиректдравклиппер:: жетклиплист**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) , слишком мал.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**ДДЕРР \_ сурфацеалреадяттачед**
</dt> <dd> <dl> <dt>



Предпринята попытка присоединить поверхность к другой поверхности, к которой она уже присоединена.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**ДДЕРР \_ сурфацеалреадидепендент**
</dt> <dd> <dl> <dt>



Была предпринята попытка сделать поверхность зависимой от другой поверхности, на которой она уже зависит.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**ДДЕРР \_ сурфацебуси**
</dt> <dd> <dl> <dt>



Отказано в доступе к поверхности, так как поверхность заблокирована другим потоком.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**ДДЕРР \_ сурфацеисобскуред**
</dt> <dd> <dl> <dt>



Отказано в доступе к поверхности, так как поверхность скрыта.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**ДДЕРР \_ сурфацелост**
</dt> <dd> <dl> <dt>



Отказано в доступе к поверхности из-за того, что память поверхности исчезла. Вызовите метод [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) на этой поверхности, чтобы восстановить связанную с ней память.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**ДДЕРР \_ сурфаценотаттачед**
</dt> <dd> <dl> <dt>



Запрошенная поверхность не присоединена.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**ДДЕРР \_ тестфинишед**
</dt> <dd> <dl> <dt>



Новое для DirectX 7,0. При возврате методом [**IDirectDraw7:: стартмодетест**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) это значение означает, что тест не может быть инициирован, так как все разрешения, выбранные для тестирования, уже содержат сведения о частоте обновления в реестре. При возврате методом [**IDirectDraw7:: евалуатемоде**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)значение означает, что DirectDraw завершил проверку частоты обновления.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**ДДЕРР \_ тубигхеигхт**
</dt> <dd> <dl> <dt>



Высота, запрошенная DirectDraw, слишком велика.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**ДДЕРР \_ тубигсизе**
</dt> <dd> <dl> <dt>



Размер, запрошенный DirectDraw, слишком велик. Однако отдельные высота и ширина являются допустимыми размерами.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**ДДЕРР \_ тубигвидс**
</dt> <dd> <dl> <dt>



Высота, запрошенная DirectDraw, слишком велика.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**ДДЕРР \_ не поддерживается**
</dt> <dd> <dl> <dt>



Операция не поддерживается.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**ДДЕРР \_ унсуппортедформат**
</dt> <dd> <dl> <dt>



Запрошенный формат пикселей не поддерживается в DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**ДДЕРР \_ унсуппортедмаск**
</dt> <dd> <dl> <dt>



Запрошенная битовая маска в формате пикселей не поддерживается в DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**ДДЕРР \_ унсуппортедмоде**
</dt> <dd> <dl> <dt>



Отображение в данный момент находится в неподдерживаемом режиме.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**ДДЕРР \_ вертикалбланкинпрогресс**
</dt> <dd> <dl> <dt>



Выполняется Вертикальное пустое поле.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**ДДЕРР \_ видеонотактиве**
</dt> <dd> <dl> <dt>



Порт видео неактивен.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**ДДЕРР \_ васстиллдравинг**
</dt> <dd> <dl> <dt>



Предыдущая операция BitBlt, которая передает информацию в эту область или из нее, является неполной.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**ДДЕРР \_ вронгмоде**
</dt> <dd> <dl> <dt>



Эту рабочую область невозможно восстановить, так как она была создана в другом режиме.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**ДДЕРР \_ ксалигн**
</dt> <dd> <dl> <dt>



Указанный прямоугольник не был горизонтально согласован по требуемой границе.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Ддрав. h</dt> </dl> |



 

