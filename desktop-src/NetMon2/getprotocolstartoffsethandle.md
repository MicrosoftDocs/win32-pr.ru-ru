---
description: Функция Жетпротоколстартоффсесандле возвращает смещение кадра для данного протокола.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Функция Жетпротоколстартоффсесандле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662181"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="19486-103">Функция Жетпротоколстартоффсесандле</span><span class="sxs-lookup"><span data-stu-id="19486-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="19486-104">Функция **жетпротоколстартоффсесандле** возвращает смещение кадра для данного протокола.</span><span class="sxs-lookup"><span data-stu-id="19486-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="19486-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19486-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="19486-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19486-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19486-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19486-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19486-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="19486-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="19486-109">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19486-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19486-110">Обработчик для протокола.</span><span class="sxs-lookup"><span data-stu-id="19486-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19486-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19486-111">Return value</span></span>

<span data-ttu-id="19486-112">Если функция выполнена успешно, возвращаемое значение является смещением кадра, измеряемого в байтах.</span><span class="sxs-lookup"><span data-stu-id="19486-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="19486-113">Если функция завершилась неудачно, возвращаемое значение равно единице (1).</span><span class="sxs-lookup"><span data-stu-id="19486-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="19486-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19486-114">Remarks</span></span>

<span data-ttu-id="19486-115">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпротоколстартоффсесандле** .</span><span class="sxs-lookup"><span data-stu-id="19486-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="19486-116">Требования</span><span class="sxs-lookup"><span data-stu-id="19486-116">Requirements</span></span>



| <span data-ttu-id="19486-117">Требование</span><span class="sxs-lookup"><span data-stu-id="19486-117">Requirement</span></span> | <span data-ttu-id="19486-118">Значение</span><span class="sxs-lookup"><span data-stu-id="19486-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19486-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19486-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19486-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19486-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="19486-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19486-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19486-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="19486-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19486-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="19486-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19486-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="19486-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="19486-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="19486-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="19486-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19486-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="19486-127">DLL</span><span class="sxs-lookup"><span data-stu-id="19486-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19486-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19486-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




