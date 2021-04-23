---
title: Коды возврата DirectDraw (Ддрав. h)
description: Ошибки представлены отрицательными значениями и не могут быть объединены.
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
ms.openlocfilehash: 7d70ff2003edc382bac2823235f01f58ffea0d91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914772"
---
# <a name="directdraw-return-codes"></a><span data-ttu-id="4fa7d-103">Коды возврата DirectDraw</span><span class="sxs-lookup"><span data-stu-id="4fa7d-103">DirectDraw Return Codes</span></span>

<span data-ttu-id="4fa7d-104">Ошибки представлены отрицательными значениями и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="4fa7d-105">В этой таблице перечислены значения, которые могут быть возвращены всеми методами [интерфейсов DirectDraw](directdraw-interfaces.md) и [функций DirectDraw](directdraw-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4fa7d-105">This table lists the values that can be returned by all methods of the [DirectDraw Interfaces](directdraw-interfaces.md) and [DirectDraw Functions](directdraw-functions.md).</span></span> <span data-ttu-id="4fa7d-106">Список кодов ошибок, которые может возвращать каждый метод или функция, см. в описании метода или функции.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-106">For a list of the error codes that each method or function can return, see the method or function description.</span></span>

<dl> <dt>

<span data-ttu-id="4fa7d-107"><span id="DD_OK"></span><span id="dd_ok"></span>**ДД \_ ОК**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-107"><span id="DD_OK"></span><span id="dd_ok"></span>**DD\_OK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-108">Запрос успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-108">The request completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**ДДЕРР \_ алреадинитиализед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-109"><span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR\_ALREADYINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-110">Объект уже инициализирован.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-110">The object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**ДДЕРР \_ блтфасткантклип**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-111"><span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR\_BLTFASTCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-112">Объект Директдравклиппер присоединяется к исходной поверхности, которая была передана в вызов метода [**IDirectDrawSurface7:: блтфаст**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .</span><span class="sxs-lookup"><span data-stu-id="4fa7d-112">A DirectDrawClipper object is attached to a source surface that has passed into a call to the [**IDirectDrawSurface7::BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**ДДЕРР \_ каннотаттачсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-113"><span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR\_CANNOTATTACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-114">Поверхность не может быть присоединена к другой запрошенной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-114">A surface cannot be attached to another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**ДДЕРР \_ каннотдетачсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-115"><span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR\_CANNOTDETACHSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-116">Поверхность не может быть отсоединена от другой запрошенной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-116">A surface cannot be detached from another requested surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**ДДЕРР \_ канткреатедк**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-117"><span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR\_CANTCREATEDC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-118">Windows не может создать больше контекстов устройств (DCs), или контроллер домена запросил область с индексированием в палитре, если у поверхности нет палитры и режим отображения не индексирован (в данном случае DirectDraw не может выбрать правильную палитру в контроллере домена).</span><span class="sxs-lookup"><span data-stu-id="4fa7d-118">Windows cannot create any more device contexts (DCs), or a DC has requested a palette-indexed surface when the surface had no palette and the display mode was not palette-indexed (in this case, DirectDraw cannot select a proper palette into the DC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**ДДЕРР \_ кантдупликате**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-119"><span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR\_CANTDUPLICATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-120">Основные и трехмерные поверхности или поверхности, созданные неявно, не могут дублироваться.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-120">Primary and 3-D surfaces, or surfaces that are implicitly created, cannot be duplicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**ДДЕРР \_ кантлокксурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-121"><span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR\_CANTLOCKSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-122">Доступ к этой поверхности отклонен, так как была предпринята попытка заблокировать основную поверхность без поддержки интерфейса управления отображением (ДЦИ).</span><span class="sxs-lookup"><span data-stu-id="4fa7d-122">Access to this surface is refused because an attempt was made to lock the primary surface without Display Control Interface (DCI) support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**ДДЕРР \_ кантпажелокк**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-123"><span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR\_CANTPAGELOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-124">Сбой попытки блокировки страницы в области.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-124">An attempt to page-lock a surface failed.</span></span> <span data-ttu-id="4fa7d-125">Блокировка страницы не работает на поверхности отображения памяти или на эмуляторе основной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-125">Page lock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**ДДЕРР \_ кантпажеунлокк**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-126"><span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR\_CANTPAGEUNLOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-127">Ошибка при разблокировании поверхности на странице.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-127">An attempt to page-unlock a surface failed.</span></span> <span data-ttu-id="4fa7d-128">Разблокировка страниц не работает на поверхности отображения памяти или на эмуляторе основной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-128">Page unlock does not work on a display-memory surface or an emulated primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**ДДЕРР \_ клипперисусингхвнд**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-129"><span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR\_CLIPPERISUSINGHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-130">Предпринята попытка задать список клипов для объекта Директдравклиппер, который уже отслеживает обработчик окна.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-130">An attempt was made to set a clip list for a DirectDrawClipper object that is already monitoring a window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**ДДЕРР \_ колоркэйнотсет**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-131"><span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR\_COLORKEYNOTSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-132">Для этой операции не указан ключ цвета источника.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-132">No source color key is specified for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**ДДЕРР \_ куррентлинотаваил**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-133"><span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR\_CURRENTLYNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-134">В настоящее время поддержка недоступна.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-134">No support is currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**ДДЕРР \_ ддскапскомплексрекуиред**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-135"><span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR\_DDSCAPSCOMPLEXREQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-136">Новое для DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-136">New for DirectX 7.0.</span></span> <span data-ttu-id="4fa7d-137">Для поверхности требуется \_ сложный флаг ддскапс.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-137">The surface requires the DDSCAPS\_COMPLEX flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**ДДЕРР \_ дкалреадикреатед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-138"><span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR\_DCALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-139">Для этой поверхности уже возвращен контекст устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="4fa7d-139">A device context (DC) has already been returned for this surface.</span></span> <span data-ttu-id="4fa7d-140">Для каждой поверхности можно получить только один контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-140">Only one DC can be retrieved for each surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>ДДЕРР \_ девицедоеснтовнсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-141"><span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR\_DEVICEDOESNTOWNSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-142">Поверхности, созданные одним устройством DirectDraw, не могут напрямую использоваться другим устройством DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-142">Surfaces created by one DirectDraw device cannot be used directly by another DirectDraw device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>ДДЕРР \_ директдравалреадикреатед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-143"><span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR\_DIRECTDRAWALREADYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-144">Объект DirectDraw, представляющий этот драйвер, уже создан для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-144">A DirectDraw object representing this driver has already been created for this process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_исключение ддерр**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-145"><span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**DDERR\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-146">При выполнении запрошенной операции было обнаружено исключение.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-146">An exception was encountered while performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**ДДЕРР \_ ексклусивемодеалреадисет**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-147"><span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR\_EXCLUSIVEMODEALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-148">Предпринята попытка установить совместный уровень, если он уже был установлен в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-148">An attempt was made to set the cooperative level when it was already set to exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**\_срок действия ддерр истек**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-149"><span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-150">Срок действия данных истек, поэтому они больше не действительны.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-150">The data has expired and is therefore no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**ДДЕРР \_ Generic**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-151"><span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-152">Неопределенное условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-152">There is an undefined error condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**ДДЕРР \_ хеигхталигн**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-153"><span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR\_HEIGHTALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-154">Высота указанного прямоугольника не кратна требуемому выравниванию.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-154">The height of the provided rectangle is not a multiple of the required alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**ДДЕРР \_ хвндалреадисет**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-155"><span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR\_HWNDALREADYSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-156">Обработчик окна с поддержкой DirectDraw-уровня уже задан.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-156">The DirectDraw cooperative-level window handle has already been set.</span></span> <span data-ttu-id="4fa7d-157">Он не может быть сброшен, пока для процесса созданы поверхности или палитры.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-157">It cannot be reset while the process has surfaces or palettes created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**ДДЕРР \_ хвндсубклассед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-158"><span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR\_HWNDSUBCLASSED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-159">DirectDraw не может восстановить состояние из-за того, что многоуровневый оконный обработчик DirectDraw является подклассом.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-159">DirectDraw is prevented from restoring state because the DirectDraw cooperative-level window handle has been subclassed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**ДДЕРР \_ имплиЦитликреатед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-160"><span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR\_IMPLICITLYCREATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-161">Невозможно восстановить поверхность, так как она является неявно созданной поверхностью.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-161">The surface cannot be restored because it is an implicitly created surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**ДДЕРР \_ инкомпатиблепримари**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-162"><span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR\_INCOMPATIBLEPRIMARY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-163">Запрос на создание основной поверхности не соответствует существующей первичной поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-163">The primary surface creation request does not match the existing primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**ДДЕРР \_ инвалидкапс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-164"><span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR\_INVALIDCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-165">Одна или несколько битов возможностей, переданных функции обратного вызова, неверны.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-165">One or more of the capability bits passed to the callback function are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**ДДЕРР \_ инвалидклиплист**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-166"><span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR\_INVALIDCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-167">DirectDraw не поддерживает указанный список клипов.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-167">DirectDraw does not support the provided clip list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**ДДЕРР \_ инвалиддиректдравгуид**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-168"><span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR\_INVALIDDIRECTDRAWGUID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-169">Глобальный уникальный идентификатор (GUID), переданный функции [**директдравкреате**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) , не является допустимым идентификатором драйвера DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-169">The globally unique identifier (GUID) passed to the [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) function is not a valid DirectDraw driver identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**ДДЕРР \_ инвалидмоде**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-170"><span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR\_INVALIDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-171">DirectDraw не поддерживает запрошенный режим.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-171">DirectDraw does not support the requested mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**ДДЕРР \_ инвалидобжект**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-172"><span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR\_INVALIDOBJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-173">DirectDraw получил указатель, который являлся недопустимым объектом DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-173">DirectDraw received a pointer that was an invalid DirectDraw object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**ДДЕРР \_ инвалидпарамс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-174"><span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR\_INVALIDPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-175">Один или несколько параметров, переданных в метод, неверны.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-175">One or more of the parameters passed to the method are incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**ДДЕРР \_ инвалидпикселформат**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-176"><span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR\_INVALIDPIXELFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-177">Формат пикселей был недопустимым, как указано.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-177">The pixel format was invalid as specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**ДДЕРР \_ инвалидпоситион**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-178"><span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR\_INVALIDPOSITION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-179">Расположение оверлея в месте назначения больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-179">The position of the overlay on the destination is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**ДДЕРР \_ инвалидрект**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-180"><span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR\_INVALIDRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-181">Указан недопустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-181">The provided rectangle was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**ДДЕРР \_ инвалидстреам**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-182"><span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR\_INVALIDSTREAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-183">Указанный поток содержит недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-183">The specified stream contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**ДДЕРР \_ инвалидсурфацетипе**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-184"><span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR\_INVALIDSURFACETYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-185">Неверный тип поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-185">The surface was of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**ДДЕРР \_ локкедсурфацес**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-186"><span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR\_LOCKEDSURFACES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-187">Одна или несколько поверхностей заблокированы, что приводит к сбою запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-187">One or more surfaces are locked, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**ДДЕРР \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-188"><span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR\_MOREDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-189">Доступно больше данных, чем может вместить указанный размер буфера.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-189">There is more data available than the specified buffer size can hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**ДДЕРР \_ использованием NewMode**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-190"><span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR\_NEWMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-191">Новое для DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-191">New for DirectX 7.0.</span></span> <span data-ttu-id="4fa7d-192">Когда [**IDirectDraw7:: стартмодетест**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) вызывается с \_ флагом ддсмт истестрекуиред, он может вернуть это значение, чтобы отметить, что некоторые или все разрешения можно и следует протестировать.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-192">When [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) is called with the DDSMT\_ISTESTREQUIRED flag, it might return this value to denote that some or all of the resolutions can and should be tested.</span></span> <span data-ttu-id="4fa7d-193">[**IDirectDraw7:: евалуатемоде**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) возвращает это значение, указывающее, что тест переключен на новый режим отображения.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-193">[**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) returns this value to indicate that the test has switched to a new display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**ДДЕРР \_ NO3D**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-194"><span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR\_NO3D**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-195">Отсутствует трехмерное оборудование или эмуляция.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-195">No 3-D hardware or emulation is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**ДДЕРР \_ ноалфахв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-196"><span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR\_NOALPHAHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-197">Оборудование с альфа-ускорением отсутствует или доступно, что приводит к сбою запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-197">No alpha-acceleration hardware is present or available, causing the failure of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**ДДЕРР \_ ноблсв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-198"><span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR\_NOBLTHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-199">Нет битового блока, поступающего в передачу.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-199">No bit block transferring hardware is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**ДДЕРР \_ ноклиплист**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-200"><span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR\_NOCLIPLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-201">Список клипов недоступен.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-201">No clip list is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**ДДЕРР \_ ноклипператтачед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-202"><span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR\_NOCLIPPERATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-203">К объекту Surface не присоединен объект Директдравклиппер.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-203">No DirectDrawClipper object is attached to the surface object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**ДДЕРР \_ ноколорконвхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-204"><span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR\_NOCOLORCONVHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-205">Оборудование для преобразования цветов отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-205">No color-conversion hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**ДДЕРР \_ ноколоркэй**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-206"><span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR\_NOCOLORKEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-207">У поверхности пока нет ключа цвета.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-207">The surface does not currently have a color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**ДДЕРР \_ ноколоркэйхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-208"><span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR\_NOCOLORKEYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-209">Отсутствует поддержка оборудования для ключа цвета назначения.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-209">There is no hardware support for the destination color key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**ДДЕРР \_ нокуперативелевелсет**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-210"><span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR\_NOCOOPERATIVELEVELSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-211">Функция Create была вызвана без метода [**IDirectDraw7:: сеткуперативелевел**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .</span><span class="sxs-lookup"><span data-stu-id="4fa7d-211">A create function was called without the [**IDirectDraw7::SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**ДДЕРР \_ нодк**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-212"><span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR\_NODC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-213">Для этой поверхности не был создан контекст устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="4fa7d-213">No device context (DC) has ever been created for this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**ДДЕРР \_ ноддропшв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-214"><span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR\_NODDROPSHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-215">Оборудование DirectDraw-Operation (верхнем) не доступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-215">No DirectDraw raster-operation (ROP) hardware is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**ДДЕРР \_ нодиректдравхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-216"><span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR\_NODIRECTDRAWHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-217">Создание объекта DirectDraw с аппаратным обеспечением невозможно; драйвер не поддерживает оборудование.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-217">Hardware-only DirectDraw object creation is not possible; the driver does not support any hardware.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**ДДЕРР \_ нодиректдравсуппорт**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-218"><span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR\_NODIRECTDRAWSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-219">Поддержка DirectDraw с текущим драйвером экрана невозможна.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-219">DirectDraw support is not possible with the current display driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**ДДЕРР \_ нодриверсуппорт**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-220"><span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR\_NODRIVERSUPPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-221">Новое для DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-221">New for DirectX 7.0.</span></span> <span data-ttu-id="4fa7d-222">Продолжение тестирования невозможно, так как драйвер видеоадаптера не перечисляет частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-222">Testing cannot proceed because the display adapter driver does not enumerate refresh rates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**\_Эмуляция ддерр**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-223"><span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR\_NOEMULATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-224">Эмуляция программного обеспечения недоступна.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-224">Software emulation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**ДДЕРР \_ ноексклусивемоде**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-225"><span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR\_NOEXCLUSIVEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-226">Для операции требуется, чтобы приложение имело монопольный режим, но приложение не имеет монопольного режима.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-226">The operation requires the application to have exclusive mode, but the application does not have exclusive mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**ДДЕРР \_ нофлифв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-227"><span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR\_NOFLIPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-228">Зеркальное отображение видимых поверхностей не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-228">Flipping visible surfaces is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**ДДЕРР \_ нофокусвиндов**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-229"><span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR\_NOFOCUSWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-230">Предпринята попытка создать или задать окно устройства без предварительного задания фокусного окна.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-230">An attempt was made to create or set a device window without first setting the focus window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**ДДЕРР \_ ногди**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-231"><span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR\_NOGDI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-232">GDI отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-232">No GDI is present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**ДДЕРР \_ HWND**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-233"><span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR\_NOHWND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-234">Для уведомления Clipper требуется обработчик окна, или ни один из окон не был ранее задан в качестве обработчика окна параллельного уровня.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-234">Clipper notification requires a window handle, or no window handle has been previously set as the cooperative level window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**ДДЕРР \_ номипмафв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-235"><span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR\_NOMIPMAPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-236">Оборудование для сопоставления текстур, поддерживающее mipmap, отсутствует или доступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-236">No mipmap-capable texture mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**ДДЕРР \_ номиррорхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-237"><span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR\_NOMIRRORHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-238">Оборудование зеркального отображения отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-238">No mirroring hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**ДДЕРР \_ номониторинформатион**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-239"><span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR\_NOMONITORINFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-240">Новое для DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-240">New for DirectX 7.0.</span></span> <span data-ttu-id="4fa7d-241">Продолжение тестирования невозможно, так как монитор не имеет связанных данных EDID.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-241">Testing cannot proceed because the monitor has no associated EDID data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**ДДЕРР \_ нононлокалвидмем**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-242"><span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR\_NONONLOCALVIDMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-243">Предпринята попытка выделить нелокальную видеопамять на устройстве, которое не поддерживает нелокальную видеопамять.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-243">An attempt was made to allocate nonlocal video memory from a device that does not support nonlocal video memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**ДДЕРР \_ нуптимизехв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-244"><span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR\_NOOPTIMIZEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-245">Устройство не поддерживает оптимизированные поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-245">The device does not support optimized surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**ДДЕРР \_ нуверлайдест**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-246"><span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR\_NOOVERLAYDEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-247">Метод [**IDirectDrawSurface7:: жетоверлайпоситион**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) вызывается для оверлея, который метод [**IDirectDrawSurface7:: упдатеоверлай**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) не вызывал для установки в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-247">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method is called on an overlay that the [**IDirectDrawSurface7::UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) method has not been called on to establish as a destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**ДДЕРР \_ нуверлайхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-248"><span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR\_NOOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-249">Оборудование оверлея отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-249">No overlay hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**ДДЕРР \_ нопалеттеаттачед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-250"><span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR\_NOPALETTEATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-251">К этой поверхности не присоединен объект палитры.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-251">No palette object is attached to this surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**ДДЕРР \_ нопалеттехв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-252"><span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR\_NOPALETTEHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-253">Отсутствует аппаратная поддержка 16-или 256-цветовых палитр.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-253">There is no hardware support for 16- or 256-color palettes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**ДДЕРР \_ норастерофв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-254"><span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR\_NORASTEROPHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-255">Соответствующее оборудование точечной операции отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-255">No appropriate raster-operation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**ДДЕРР \_ норотатионхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-256"><span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR\_NOROTATIONHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-257">Оборудование для вращения отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-257">No rotation hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**ДДЕРР \_ ностереохардваре**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-258"><span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR\_NOSTEREOHARDWARE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-259">Стерео оборудование отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-259">There is no stereo hardware present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**ДДЕРР \_ ностретчхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-260"><span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR\_NOSTRETCHHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-261">Аппаратная поддержка для растяжения отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-261">There is no hardware support for stretching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**ДДЕРР \_ носурфацелефт**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-262"><span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR\_NOSURFACELEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-263">Отсутствует оборудование, поддерживающее стерео поверхности.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-263">There is no hardware present that supports stereo surfaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**ДДЕРР \_ NOT4BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-264"><span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR\_NOT4BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-265">Объект Директдравсурфаце не использует 4-разрядную цветовую палитру, и для выполнения запрошенной операции требуется 4-разрядная цветовая палитра.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-265">The DirectDrawSurface object is not using a 4-bit color palette, and the requested operation requires a 4-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**ДДЕРР \_ NOT4BITCOLORINDEX**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-266"><span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR\_NOT4BITCOLORINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-267">Объект Директдравсурфаце не использует 4-разрядную палитру индекса цвета, и для запрошенной операции требуется 4-разрядная палитра индекса цвета.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-267">The DirectDrawSurface object is not using a 4-bit color index palette, and the requested operation requires a 4-bit color index palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**ДДЕРР \_ NOT8BITCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-268"><span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR\_NOT8BITCOLOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-269">Объект Директдравсурфаце не использует 8-разрядную цветовую палитру, и для выполнения запрошенной операции требуется 8-разрядная цветовая палитра.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-269">The DirectDrawSurface object is not using an 8-bit color palette, and the requested operation requires an 8-bit color palette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**ДДЕРР \_ нотаоверлайсурфаце**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-270"><span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR\_NOTAOVERLAYSURFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-271">Для неналоженной поверхности вызывается компонент оверлея.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-271">An overlay component is called for a nonoverlay surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**ДДЕРР \_ нотекстурехв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-272"><span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR\_NOTEXTUREHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-273">Операция не может быть выполнена, так как оборудование для сопоставления текстур отсутствует или недоступно.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-273">The operation cannot be carried out because no texture-mapping hardware is present or available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**ДДЕРР \_ нотфлиппабле**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-274"><span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR\_NOTFLIPPABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-275">Предпринята попытка перевернуть поверхность, которая не может быть отражена.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-275">An attempt was made to flip a surface that cannot be flipped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**ДДЕРР \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-276"><span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-277">Запрашиваемый элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-277">The requested item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**ДДЕРР \_ нотинитиализед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-278"><span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR\_NOTINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-279">Была предпринята попытка вызвать метод интерфейса объекта DirectDraw, созданного функцией [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) до инициализации объекта.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-279">An attempt was made to call an interface method of a DirectDraw object created by [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) before the object was initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**ДДЕРР \_ загружен»**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-280"><span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR\_NOTLOADED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-281">Поверхность — это оптимизированная поверхность, но она пока не выделила память.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-281">The surface is an optimized surface, but it has not yet been allocated any memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**ДДЕРР \_ нотлоккед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-282"><span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR\_NOTLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-283">Предпринята попытка разблокировать незаблокированную поверхность.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-283">An attempt was made to unlock a surface that was not locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**ДДЕРР \_ нотпажелоккед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-284"><span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR\_NOTPAGELOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-285">Была предпринята попытка разблокировки поверхности без необработанных блокировок страниц.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-285">An attempt was made to page-unlock a surface with no outstanding page locks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**ДДЕРР \_ нотпалеттизед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-286"><span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR\_NOTPALETTIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-287">Используемая поверхность не является поверхностью на основе палитры.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-287">The surface being used is not a palette-based surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**ДДЕРР \_ новсинчв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-288"><span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR\_NOVSYNCHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-289">Аппаратная поддержка вертикальных пустых синхронизированных операций не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-289">There is no hardware support for vertical blank synchronized operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**ДДЕРР \_ нозбуфферхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-290"><span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR\_NOZBUFFERHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-291">Операция создания z-буфера в отображаемой памяти или выполнения блочного блока (BitBlt) с помощью z-буфера не может быть выполнена, так как отсутствует поддержка аппаратных буферов z.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-291">The operation to create a z-buffer in display memory or to perform a bit block transfer (bitblt), using a z-buffer cannot be carried out because there is no hardware support for z-buffers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**ДДЕРР \_ нозоверлайхв**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-292"><span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR\_NOZOVERLAYHW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-293">Поверхности наложения не могут быть z-слоями на основе z-порядка, так как оборудование не поддерживает z-порядок наложений.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-293">The overlay surfaces cannot be z-layered, based on the z-order because the hardware does not support z-ordering of overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**ДДЕРР \_ аутофкапс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-294"><span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR\_OUTOFCAPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-295">Оборудование, необходимое для запрошенной операции, уже выделено.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-295">The hardware needed for the requested operation has already been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**ДДЕРР \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-296"><span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**DDERR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-297">DirectDraw не хватает памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-297">DirectDraw does not have enough memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**ДДЕРР \_ аутофвидеомемори**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-298"><span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR\_OUTOFVIDEOMEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-299">DirectDraw не имеет достаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-299">DirectDraw does not have enough display memory to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**ДДЕРР \_ оверлаппингректс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-300"><span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR\_OVERLAPPINGRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-301">Исходный и конечный прямоугольники находятся на одной поверхности и перекрываются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-301">The source and destination rectangles are on the same surface and overlap each other.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**ДДЕРР \_ оверлайкантклип**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-302"><span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR\_OVERLAYCANTCLIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-303">Оборудование не поддерживает обрезанные наложения.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-303">The hardware does not support clipped overlays.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**ДДЕРР \_ оверлайколоркэйонлйонеактиве**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-304"><span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR\_OVERLAYCOLORKEYONLYONEACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-305">Предпринята попытка активировать более одного цвета ключа на наложении.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-305">An attempt was made to have more than one color key active on an overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**ДДЕРР \_ оверлайнотвисибле**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-306"><span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR\_OVERLAYNOTVISIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-307">Метод [**IDirectDrawSurface7:: жетоверлайпоситион**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) был вызван для скрытого оверлея.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-307">The [**IDirectDrawSurface7::GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) method was called on a hidden overlay.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**ДДЕРР \_ палеттебуси**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-308"><span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR\_PALETTEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-309">Доступ к этой палитре отклонен, так как палитра заблокирована другим потоком.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-309">Access to this palette is refused because the palette is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**ДДЕРР \_ примарисурфацеалреадексистс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-310"><span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR\_PRIMARYSURFACEALREADYEXISTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-311">Этот процесс уже создал основную поверхность.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-311">This process has already created a primary surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**ДДЕРР \_ регионтусмалл**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-312"><span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR\_REGIONTOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-313">Регион, переданный методу [**идиректдравклиппер:: жетклиплист**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-313">The region passed to the [**IDirectDrawClipper::GetClipList**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) method is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**ДДЕРР \_ сурфацеалреадяттачед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-314"><span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR\_SURFACEALREADYATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-315">Предпринята попытка присоединить поверхность к другой поверхности, к которой она уже присоединена.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-315">An attempt was made to attach a surface to another surface to which it is already attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**ДДЕРР \_ сурфацеалреадидепендент**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-316"><span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR\_SURFACEALREADYDEPENDENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-317">Была предпринята попытка сделать поверхность зависимой от другой поверхности, на которой она уже зависит.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-317">An attempt was made to make a surface a dependency of another surface on which it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**ДДЕРР \_ сурфацебуси**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-318"><span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR\_SURFACEBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-319">Отказано в доступе к поверхности, так как поверхность заблокирована другим потоком.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-319">Access to the surface is refused because the surface is locked by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**ДДЕРР \_ сурфацеисобскуред**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-320"><span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR\_SURFACEISOBSCURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-321">Отказано в доступе к поверхности, так как поверхность скрыта.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-321">Access to the surface is refused because the surface is obscured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**ДДЕРР \_ сурфацелост**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-322"><span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR\_SURFACELOST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-323">Отказано в доступе к поверхности из-за того, что память поверхности исчезла.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-323">Access to the surface is refused because the surface memory is gone.</span></span> <span data-ttu-id="4fa7d-324">Вызовите метод [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) на этой поверхности, чтобы восстановить связанную с ней память.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-324">Call the [**IDirectDrawSurface7::Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) method on this surface to restore the memory associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**ДДЕРР \_ сурфаценотаттачед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-325"><span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR\_SURFACENOTATTACHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-326">Запрошенная поверхность не присоединена.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-326">The requested surface is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**ДДЕРР \_ тестфинишед**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-327"><span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR\_TESTFINISHED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-328">Новое для DirectX 7,0.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-328">New for DirectX 7.0.</span></span> <span data-ttu-id="4fa7d-329">При возврате методом [**IDirectDraw7:: стартмодетест**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) это значение означает, что тест не может быть инициирован, так как все разрешения, выбранные для тестирования, уже содержат сведения о частоте обновления в реестре.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-329">When returned by the [**IDirectDraw7::StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) method, this value means that no test could be initiated because all the resolutions chosen for testing already have refresh rate information in the registry.</span></span> <span data-ttu-id="4fa7d-330">При возврате методом [**IDirectDraw7:: евалуатемоде**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode)значение означает, что DirectDraw завершил проверку частоты обновления.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-330">When returned by [**IDirectDraw7::EvaluateMode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), the value means that DirectDraw has completed a refresh rate test.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**ДДЕРР \_ тубигхеигхт**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-331"><span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR\_TOOBIGHEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-332">Высота, запрошенная DirectDraw, слишком велика.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-332">The height requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**ДДЕРР \_ тубигсизе**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-333"><span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR\_TOOBIGSIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-334">Размер, запрошенный DirectDraw, слишком велик.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-334">The size requested by DirectDraw is too large.</span></span> <span data-ttu-id="4fa7d-335">Однако отдельные высота и ширина являются допустимыми размерами.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-335">However, the individual height and width are valid sizes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**ДДЕРР \_ тубигвидс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-336"><span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR\_TOOBIGWIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-337">Высота, запрошенная DirectDraw, слишком велика.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-337">The width requested by DirectDraw is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**ДДЕРР \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-338"><span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-339">Операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-339">The operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**ДДЕРР \_ унсуппортедформат**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-340"><span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR\_UNSUPPORTEDFORMAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-341">Запрошенный формат пикселей не поддерживается в DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-341">The pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**ДДЕРР \_ унсуппортедмаск**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-342"><span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR\_UNSUPPORTEDMASK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-343">Запрошенная битовая маска в формате пикселей не поддерживается в DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-343">The bitmask in the pixel format requested is not supported by DirectDraw.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**ДДЕРР \_ унсуппортедмоде**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-344"><span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR\_UNSUPPORTEDMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-345">Отображение в данный момент находится в неподдерживаемом режиме.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-345">The display is currently in an unsupported mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**ДДЕРР \_ вертикалбланкинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-346"><span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR\_VERTICALBLANKINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-347">Выполняется Вертикальное пустое поле.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-347">A vertical blank is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**ДДЕРР \_ видеонотактиве**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-348"><span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR\_VIDEONOTACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-349">Порт видео неактивен.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-349">The video port is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**ДДЕРР \_ васстиллдравинг**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-350"><span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR\_WASSTILLDRAWING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-351">Предыдущая операция BitBlt, которая передает информацию в эту область или из нее, является неполной.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-351">The previous bitblt operation that is transferring information to or from this surface is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**ДДЕРР \_ вронгмоде**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-352"><span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR\_WRONGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-353">Эту рабочую область невозможно восстановить, так как она была создана в другом режиме.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-353">This surface cannot be restored because it was created in a different mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fa7d-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**ДДЕРР \_ ксалигн**</span><span class="sxs-lookup"><span data-stu-id="4fa7d-354"><span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR\_XALIGN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fa7d-355">Указанный прямоугольник не был горизонтально согласован по требуемой границе.</span><span class="sxs-lookup"><span data-stu-id="4fa7d-355">The provided rectangle was not horizontally aligned on a required boundary.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fa7d-356">Требования</span><span class="sxs-lookup"><span data-stu-id="4fa7d-356">Requirements</span></span>



| <span data-ttu-id="4fa7d-357">Требование</span><span class="sxs-lookup"><span data-stu-id="4fa7d-357">Requirement</span></span> | <span data-ttu-id="4fa7d-358">Значение</span><span class="sxs-lookup"><span data-stu-id="4fa7d-358">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa7d-359">Header</span><span class="sxs-lookup"><span data-stu-id="4fa7d-359">Header</span></span><br/> | <dl> <span data-ttu-id="4fa7d-360"><dt>Ддрав. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa7d-360"><dt>Ddraw.h</dt></span></span> </dl> |



 

