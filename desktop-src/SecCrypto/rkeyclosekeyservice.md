---
description: Функция Ркэйклосекэйсервице не поддерживается.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Функция Ркэйклосекэйсервице (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897390"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="7e198-103">Функция Ркэйклосекэйсервице</span><span class="sxs-lookup"><span data-stu-id="7e198-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="7e198-104">Функция **ркэйклосекэйсервице** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e198-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="7e198-105">**Windows Server 2003:** Функция **ркэйклосекэйсервице** закрывает маркер службы ключа, Открытый с помощью предыдущего вызова функции [**ркэйопенкэйсервице**](rkeyopenkeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7e198-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="7e198-106">Обратите внимание, что это поведение изменилось в Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7e198-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e198-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e198-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="7e198-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e198-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e198-109">*хкэйсвккли* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e198-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e198-110">Обработчик [**\_ обработчика кэйсвкк**](keysvcc-handle.md) , который ранее открывался [**ркэйопенкэйсервице**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="7e198-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="7e198-111">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e198-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7e198-112">*сохраняется* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7e198-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e198-113">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7e198-113">Reserved.</span></span> <span data-ttu-id="7e198-114">Присвойте этому параметру значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7e198-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e198-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e198-115">Return value</span></span>

<span data-ttu-id="7e198-116">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7e198-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="7e198-117">Если функция завершается ошибкой, возвращается значение типа **ulong** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="7e198-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e198-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7e198-118">Requirements</span></span>



| <span data-ttu-id="7e198-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7e198-119">Requirement</span></span> | <span data-ttu-id="7e198-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7e198-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e198-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e198-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e198-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7e198-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="7e198-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e198-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e198-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e198-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e198-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e198-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e198-126"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e198-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e198-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e198-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e198-128">**ркэйопенкэйсервице**</span><span class="sxs-lookup"><span data-stu-id="7e198-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="7e198-129">**ркэйпфксинсталл**</span><span class="sxs-lookup"><span data-stu-id="7e198-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




