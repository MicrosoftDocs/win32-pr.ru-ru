---
title: Функция Вссетаутофаил (Вебсервицесдебуг. h)
description: Задает следующую точку для внедрения сбоя. Это функция только для отладки.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Веб-службы Вссетаутофаил Function для Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534925"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="8a0b5-105">Функция Вссетаутофаил</span><span class="sxs-lookup"><span data-stu-id="8a0b5-105">WsSetAutoFail function</span></span>

<span data-ttu-id="8a0b5-106">Задает следующую точку для внедрения сбоя.</span><span class="sxs-lookup"><span data-stu-id="8a0b5-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="8a0b5-107">Это функция только для отладки.</span><span class="sxs-lookup"><span data-stu-id="8a0b5-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0b5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a0b5-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="8a0b5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a0b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0b5-110">*количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a0b5-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0b5-111">Указывает, сколько операций должно быть выполнено до начала ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a0b5-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="8a0b5-112">*Ошибка при* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8a0b5-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0b5-113">Указатель на объект [ \_ ошибки WS](ws-error.md) , в котором необходимо сохранить дополнительные сведения об ошибке в случае сбоя функции.</span><span class="sxs-lookup"><span data-stu-id="8a0b5-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0b5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a0b5-114">Return value</span></span>

<span data-ttu-id="8a0b5-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8a0b5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a0b5-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a0b5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0b5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8a0b5-117">Requirements</span></span>



| <span data-ttu-id="8a0b5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8a0b5-118">Requirement</span></span> | <span data-ttu-id="8a0b5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8a0b5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0b5-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a0b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0b5-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8a0b5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a0b5-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a0b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0b5-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a0b5-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8a0b5-124">Header</span><span class="sxs-lookup"><span data-stu-id="8a0b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a0b5-125"><dt>Вебсервицесдебуг. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0b5-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





