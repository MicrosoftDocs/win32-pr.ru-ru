---
title: Методы свойств Иадспринткуеуеоператионс (iAds. h)
description: Методы свойств интерфейса Иадспринткуеуеоператионс считывают и записывают свойства, перечисленные в следующем списке. Дополнительные сведения о методах свойств см. в разделе методы свойств интерфейса.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспринткуеуеоператионс ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989091"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="82290-105">Методы свойств Иадспринткуеуеоператионс</span><span class="sxs-lookup"><span data-stu-id="82290-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="82290-106">Методы свойств интерфейса [**иадспринткуеуеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) считывают и записывают свойства, перечисленные в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="82290-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="82290-107">Дополнительные сведения о методах свойств см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="82290-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="82290-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="82290-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="82290-109">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="82290-109">**Status**</span></span>
<span data-ttu-id="82290-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="82290-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="82290-111">Текущее состояние операций очереди печати.</span><span class="sxs-lookup"><span data-stu-id="82290-111">Current status of the print queue operations.</span></span> <span data-ttu-id="82290-112">Допустимые значения кода состояния перечислены в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="82290-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="82290-113">**Реклама \_ ПРИНТЕР \_ приостановлен** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="82290-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="82290-114">**Реклама \_ \_Ожидание \_ удаления принтера** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="82290-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="82290-115">**Реклама \_ \_Ошибка принтера** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="82290-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="82290-116">**Реклама \_ \_ \_ Застревание бумаги в принтере** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="82290-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="82290-117">**Реклама \_ \_ \_ Выходной документ принтера** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="82290-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="82290-118">**Реклама \_ \_Ручной \_ веб-канал принтера** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="82290-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="82290-119">**Реклама \_ \_ \_ Проблема с принтером** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="82290-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="82290-120">**Реклама \_ \_Автономный принтер** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="82290-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="82290-121">**Реклама \_ \_ \_ Активный ввод-вывод принтера** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="82290-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="82290-122">**Реклама \_ ПРИНТЕР \_ занят** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="82290-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="82290-123">**Реклама \_ \_Печать принтера** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="82290-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="82290-124">**Реклама \_ \_Выходной \_ лоток принтера \_ полон** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="82290-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="82290-125">**Реклама \_ ПРИНТЕР \_ \_ недоступен** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="82290-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="82290-126">**Реклама \_ \_Ожидание печати** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="82290-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="82290-127">**Реклама \_ \_Обработка принтера** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="82290-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="82290-128">**Реклама \_ \_Инициализация принтера** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="82290-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="82290-129">**Реклама \_ \_Прогрев принтера \_** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="82290-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="82290-130">**Реклама \_ \_ \_ Мало тонера принтера** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="82290-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="82290-131">**Реклама \_ ПРИНТЕР \_ без \_ тонера** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="82290-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="82290-132">**Реклама \_ \_Страница принтера \_ : разрыв страницы** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="82290-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="82290-133">**Реклама \_ \_ \_ Вмешательство пользователя принтера** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="82290-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="82290-134">**Реклама \_ \_ \_ \_ Неиспользуемая память принтера** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="82290-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="82290-135">**Реклама \_ \_ \_ Открыта дверца принтера** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="82290-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="82290-136">**Реклама \_ \_Сервер принтера \_ неизвестен** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="82290-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="82290-137">**Реклама \_ \_Режим энергосбережения \_ принтера** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="82290-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="82290-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="82290-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="82290-139">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="82290-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="82290-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="82290-140">Examples</span></span>

<span data-ttu-id="82290-141">В следующем Visual Basic примере кода проверяется, что принтер застрял.</span><span class="sxs-lookup"><span data-stu-id="82290-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="82290-142">В следующем примере кода C++ проверяется Застревание принтера.</span><span class="sxs-lookup"><span data-stu-id="82290-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="82290-143">Требования</span><span class="sxs-lookup"><span data-stu-id="82290-143">Requirements</span></span>



| <span data-ttu-id="82290-144">Требование</span><span class="sxs-lookup"><span data-stu-id="82290-144">Requirement</span></span> | <span data-ttu-id="82290-145">Значение</span><span class="sxs-lookup"><span data-stu-id="82290-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="82290-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82290-146">Minimum supported client</span></span><br/> | <span data-ttu-id="82290-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82290-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="82290-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82290-148">Minimum supported server</span></span><br/> | <span data-ttu-id="82290-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82290-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="82290-150">Header</span><span class="sxs-lookup"><span data-stu-id="82290-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="82290-151"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="82290-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="82290-152">DLL</span><span class="sxs-lookup"><span data-stu-id="82290-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82290-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82290-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="82290-154">IID</span><span class="sxs-lookup"><span data-stu-id="82290-154">IID</span></span><br/>                      | <span data-ttu-id="82290-155">IID \_ иадспринткуеуеоператионс определен как 124BE5C0-156E-11CF-A986-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="82290-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82290-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82290-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82290-157">**иадспринткуеуе**</span><span class="sxs-lookup"><span data-stu-id="82290-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="82290-158">**иадспринткуеуеоператионс**</span><span class="sxs-lookup"><span data-stu-id="82290-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





