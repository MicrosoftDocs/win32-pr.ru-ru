---
title: Сообщение MM_MCISIGNAL (Ммсистем. h)
description: '\_Сообщение МЦИСИГНАЛ mm отправляется в окно для уведомления приложения о том, что устройство MCI достигло места, определенного в предыдущей команде сигнала (MCI \_ Signal).'
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415896"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="00a83-104">MM \_ мЦисигнал, сообщение</span><span class="sxs-lookup"><span data-stu-id="00a83-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="00a83-105">Сообщение **\_ мЦисигнал mm** отправляется в окно для уведомления приложения о том, что устройство MCI достигло места, определенного в предыдущей команде [**сигнала**](signal.md) ( [**MCI \_ Signal**](mci-signal.md)).</span><span class="sxs-lookup"><span data-stu-id="00a83-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="00a83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a83-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="00a83-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="00a83-108">Идентификатор устройства, запускающего сигнальное сообщение.</span><span class="sxs-lookup"><span data-stu-id="00a83-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="00a83-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*лусерпарм*</span><span class="sxs-lookup"><span data-stu-id="00a83-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="00a83-110">Значение, передаваемое в **двусерпарм** элемент структуры **\_ \_ \_ параметров сигнала MCI ДГВ** , когда команда **сигнала** определила эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="00a83-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="00a83-111">Кроме того, в нем может содержаться значение расположения.</span><span class="sxs-lookup"><span data-stu-id="00a83-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00a83-112">Требования</span><span class="sxs-lookup"><span data-stu-id="00a83-112">Requirements</span></span>



| <span data-ttu-id="00a83-113">Требование</span><span class="sxs-lookup"><span data-stu-id="00a83-113">Requirement</span></span> | <span data-ttu-id="00a83-114">Значение</span><span class="sxs-lookup"><span data-stu-id="00a83-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a83-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00a83-115">Minimum supported client</span></span><br/> | <span data-ttu-id="00a83-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00a83-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00a83-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00a83-117">Minimum supported server</span></span><br/> | <span data-ttu-id="00a83-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00a83-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00a83-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="00a83-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a83-120"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00a83-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a83-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00a83-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a83-122">MCI</span><span class="sxs-lookup"><span data-stu-id="00a83-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="00a83-123">Сообщения MCI</span><span class="sxs-lookup"><span data-stu-id="00a83-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="00a83-124">**имел**</span><span class="sxs-lookup"><span data-stu-id="00a83-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





