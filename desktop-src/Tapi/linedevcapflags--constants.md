---
description: '\_Константы битовой флага линедевкапфлагс — это коллекция логических значений, описывающих различные возможности устройств.'
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Константы LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679880"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="da0fe-103">\_Константы линедевкапфлагс</span><span class="sxs-lookup"><span data-stu-id="da0fe-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="da0fe-104">Константы битовой флага **линедевкапфлагс \_** — это коллекция логических значений, описывающих различные возможности устройств.</span><span class="sxs-lookup"><span data-stu-id="da0fe-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="da0fe-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**ЛИНЕДЕВКАПФЛАГС \_ каллхуб**</span><span class="sxs-lookup"><span data-stu-id="da0fe-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-106">Указывает, поддерживаются ли в этой строке концентраторы вызовов.</span><span class="sxs-lookup"><span data-stu-id="da0fe-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="da0fe-107">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="da0fe-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**ЛИНЕДЕВКАПФЛАГС \_ каллхубтраккинг**</span><span class="sxs-lookup"><span data-stu-id="da0fe-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-109">Указывает, поддерживается ли отслеживание концентратора вызовов в этой строке.</span><span class="sxs-lookup"><span data-stu-id="da0fe-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="da0fe-110">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="da0fe-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**ЛИНЕДЕВКАПФЛАГС \_ клоседроп**</span><span class="sxs-lookup"><span data-stu-id="da0fe-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-112">Указывает, что происходит, когда открытая строка закрывается, пока приложение вызывает активное в строке.</span><span class="sxs-lookup"><span data-stu-id="da0fe-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="da0fe-113">Если **значение — true**, поставщик услуг сбрасывает (очищает) все активные вызовы в строке, когда последнее приложение, открывшее строку, закрывает его с помощью [**линеклосе**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span><span class="sxs-lookup"><span data-stu-id="da0fe-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="da0fe-114">Если **значение равно false**, то поставщик услуг не удаляет активные вызовы в таких случаях.</span><span class="sxs-lookup"><span data-stu-id="da0fe-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="da0fe-115">Вместо этого вызовы остаются активными и управляют внешними устройствами.</span><span class="sxs-lookup"><span data-stu-id="da0fe-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="da0fe-116">Поставщик услуг обычно задает для этого бита **значение false** , если имеется другое устройство, которое может поддерживать вызов, например, если для аналоговой линии задано, что компьютер и телефон устанавливаются одновременно с подключением к ним в конфигурации, то телефон оффхук автоматически сохранит вызов активным даже после отключения компьютера.</span><span class="sxs-lookup"><span data-stu-id="da0fe-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="da0fe-117">Приложения должны установить этот флаг, чтобы определить, следует ли предупредить пользователя (с помощью диалогового окна ОК или Отмена), что активные вызовы будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="da0fe-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**ЛИНЕДЕВКАПФЛАГС \_ кроссаддрконф**</span><span class="sxs-lookup"><span data-stu-id="da0fe-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-119">Указывает, можно ли выполнить конференцию для вызовов по разным адресам в этой строке.</span><span class="sxs-lookup"><span data-stu-id="da0fe-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалбиллинг**</span><span class="sxs-lookup"><span data-stu-id="da0fe-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалдиалтоне**</span><span class="sxs-lookup"><span data-stu-id="da0fe-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**ЛИНЕДЕВКАПФЛАГС \_ диалкуиет**</span><span class="sxs-lookup"><span data-stu-id="da0fe-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-123">Эти флаги указывают, поддерживается ли модификатор строки "$", "@" или "W", поддерживающий набор строк, для данного устройства линии.</span><span class="sxs-lookup"><span data-stu-id="da0fe-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="da0fe-124">Имеет **значение true** , если модификатор поддерживается; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="da0fe-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="da0fe-125">"?" (предлагать пользователю продолжить набор) никогда не поддерживается линейным устройством.</span><span class="sxs-lookup"><span data-stu-id="da0fe-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="da0fe-126">Эти флаги позволяют приложению определить, какие модификаторы приведут к созданию ЛИНИРР.</span><span class="sxs-lookup"><span data-stu-id="da0fe-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="da0fe-127">Приложение имеет выбор предварительно сканируемых строк для неподдерживаемых символов или передачи "необработанных" строк из [**линетранслатеаддресс**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) непосредственно поставщику в составе таких функций, как [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) или [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial) , и позволить функции генерировать ошибку, чтобы сообщить ему, какой неподдерживаемый модификатор находится в строке первым.</span><span class="sxs-lookup"><span data-stu-id="da0fe-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**ЛИНЕДЕВКАПФЛАГС \_ хигхлевкомп**</span><span class="sxs-lookup"><span data-stu-id="da0fe-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-129">Указывает, поддерживаются ли в этой строке элементы сведений высокого уровня совместимости.</span><span class="sxs-lookup"><span data-stu-id="da0fe-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**ЛИНЕДЕВКАПФЛАГС \_ ловлевкомп**</span><span class="sxs-lookup"><span data-stu-id="da0fe-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-131">Указывает, поддерживаются ли в этой строке элементы сведений о совместимости низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="da0fe-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**ЛИНЕДЕВКАПФЛАГС \_ медиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="da0fe-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-133">Указывает, доступны ли операции управления мультимедиа для вызовов в этой строке.</span><span class="sxs-lookup"><span data-stu-id="da0fe-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**ЛИНЕДЕВКАПФЛАГС \_ MSP**</span><span class="sxs-lookup"><span data-stu-id="da0fe-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-135">Указывает, связана ли с линией поставщик службы мультимедиа (MSP).</span><span class="sxs-lookup"><span data-stu-id="da0fe-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="da0fe-136">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="da0fe-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**ЛИНЕДЕВКАПФЛАГС \_ мултиплеаддр**</span><span class="sxs-lookup"><span data-stu-id="da0fe-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-138">Указывает, могут ли [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**тспи \_ линемакекалл**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)или [**тспи \_ линедиал**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) работать с несколькими адресами одновременно (как для обратного мультиплексирования).</span><span class="sxs-lookup"><span data-stu-id="da0fe-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da0fe-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**ЛИНЕДЕВКАПФЛАГС \_ приватеобжектс**</span><span class="sxs-lookup"><span data-stu-id="da0fe-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da0fe-140">Указывает, реализованы ли [интерфейсы, зависящие от поставщика](./provider-specific-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="da0fe-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="da0fe-141">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="da0fe-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da0fe-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da0fe-142">Remarks</span></span>

<span data-ttu-id="da0fe-143">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="da0fe-143">No extensibility.</span></span> <span data-ttu-id="da0fe-144">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="da0fe-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0fe-145">Требования</span><span class="sxs-lookup"><span data-stu-id="da0fe-145">Requirements</span></span>



| <span data-ttu-id="da0fe-146">Требование</span><span class="sxs-lookup"><span data-stu-id="da0fe-146">Requirement</span></span> | <span data-ttu-id="da0fe-147">Значение</span><span class="sxs-lookup"><span data-stu-id="da0fe-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="da0fe-148">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="da0fe-148">TAPI version</span></span><br/> | <span data-ttu-id="da0fe-149">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="da0fe-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="da0fe-150">Header</span><span class="sxs-lookup"><span data-stu-id="da0fe-150">Header</span></span><br/>       | <dl> <span data-ttu-id="da0fe-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0fe-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0fe-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da0fe-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0fe-153">**линеклосе**</span><span class="sxs-lookup"><span data-stu-id="da0fe-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="da0fe-154">**линедиал**</span><span class="sxs-lookup"><span data-stu-id="da0fe-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="da0fe-155">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="da0fe-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="da0fe-156">**линетранслатеаддресс**</span><span class="sxs-lookup"><span data-stu-id="da0fe-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

