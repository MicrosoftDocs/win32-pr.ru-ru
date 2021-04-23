---
title: Команда MCI_CLOSE (Ммсистем. h)
description: Команда MCI \_ Close освобождает доступ к устройству или файлу. Все устройства распознают эту команду.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135678"
---
# <a name="mci_close-command"></a><span data-ttu-id="5404f-105">\_Команда «закрыть» MCI</span><span class="sxs-lookup"><span data-stu-id="5404f-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="5404f-106">Команда MCI \_ Close освобождает доступ к устройству или файлу.</span><span class="sxs-lookup"><span data-stu-id="5404f-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="5404f-107">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="5404f-107">All devices recognize this command.</span></span>

<span data-ttu-id="5404f-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="5404f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="5404f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5404f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5404f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="5404f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="5404f-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5404f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="5404f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5404f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="5404f-113">\_Ожидание с уведомлением MCI или MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="5404f-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="5404f-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5404f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5404f-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*лпклосе*</span><span class="sxs-lookup"><span data-stu-id="5404f-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="5404f-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="5404f-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="5404f-117">(Можно также использовать структуру **пармс для \_ окна \_ MCI** .</span><span class="sxs-lookup"><span data-stu-id="5404f-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="5404f-118">Дополнительные сведения см. в комментариях для **MCI \_ Generic \_ пармс**.)</span><span class="sxs-lookup"><span data-stu-id="5404f-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5404f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5404f-119">Return Value</span></span>

<span data-ttu-id="5404f-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5404f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5404f-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5404f-121">Remarks</span></span>

<span data-ttu-id="5404f-122">Выход из приложения без закрытия всех открытых устройств MCI может привести к недоступности устройства.</span><span class="sxs-lookup"><span data-stu-id="5404f-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="5404f-123">Приложение должно явным образом закрыть каждое устройство или файл после его завершения.</span><span class="sxs-lookup"><span data-stu-id="5404f-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="5404f-124">MCI выгружает устройство при закрытии всех экземпляров устройства или всех связанных с ним файлов.</span><span class="sxs-lookup"><span data-stu-id="5404f-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5404f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5404f-125">Requirements</span></span>



| <span data-ttu-id="5404f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5404f-126">Requirement</span></span> | <span data-ttu-id="5404f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5404f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5404f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5404f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5404f-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5404f-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5404f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5404f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5404f-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5404f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5404f-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5404f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5404f-133"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5404f-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5404f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5404f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5404f-135">MCI</span><span class="sxs-lookup"><span data-stu-id="5404f-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5404f-136">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="5404f-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

