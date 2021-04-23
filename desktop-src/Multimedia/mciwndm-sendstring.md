---
title: Сообщение MCIWNDM_SENDSTRING (VFW. h)
description: Сообщение МЦИВНДМ \_ сендстринг отправляет команду MCI в виде строки на устройство, связанное с окном мЦивнд. Это сообщение можно отправить явно или с помощью макроса МЦивндсендстринг.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803016"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="31b80-105">\_Сообщение мЦивндм сендстринг</span><span class="sxs-lookup"><span data-stu-id="31b80-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="31b80-106">Сообщение **мЦивндм \_ сендстринг** отправляет команду MCI в виде строки на устройство, связанное с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="31b80-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="31b80-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсендстринг**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .</span><span class="sxs-lookup"><span data-stu-id="31b80-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="31b80-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31b80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b80-109"><span id="sz"></span><span id="SZ"></span>*SZ*</span><span class="sxs-lookup"><span data-stu-id="31b80-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="31b80-110">Строка команды для отправки на устройство MCI.</span><span class="sxs-lookup"><span data-stu-id="31b80-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b80-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31b80-111">Return Value</span></span>

<span data-ttu-id="31b80-112">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="31b80-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="31b80-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31b80-113">Remarks</span></span>

<span data-ttu-id="31b80-114">Обработчик сообщений для **мЦивндм \_ сендстринг** добавляет псевдоним устройства к команде MCI, отправляемой на устройство.</span><span class="sxs-lookup"><span data-stu-id="31b80-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="31b80-115">Поэтому не следует использовать псевдоним в команде MCI, которую вы выпустили с помощью **мЦивндм \_ сендстринг**.</span><span class="sxs-lookup"><span data-stu-id="31b80-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="31b80-116">Чтобы получить возвращаемую строку, которая содержит результат выполнения команды, отправьте сообщение [**мЦивндм \_ ретурнстринг**](mciwndm-returnstring.md) .</span><span class="sxs-lookup"><span data-stu-id="31b80-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="31b80-117">Требования</span><span class="sxs-lookup"><span data-stu-id="31b80-117">Requirements</span></span>



| <span data-ttu-id="31b80-118">Требование</span><span class="sxs-lookup"><span data-stu-id="31b80-118">Requirement</span></span> | <span data-ttu-id="31b80-119">Значение</span><span class="sxs-lookup"><span data-stu-id="31b80-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="31b80-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31b80-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31b80-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31b80-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="31b80-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31b80-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31b80-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="31b80-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="31b80-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="31b80-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b80-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b80-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b80-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31b80-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b80-127">**мЦивндсендстринг**</span><span class="sxs-lookup"><span data-stu-id="31b80-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="31b80-128">Строки команд мультимедиа</span><span class="sxs-lookup"><span data-stu-id="31b80-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





