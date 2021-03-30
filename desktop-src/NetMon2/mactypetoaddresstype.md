---
description: Функция Мактипетоаддресстипе преобразует данный тип MAC в тип адреса.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Функция Мактипетоаддресстипе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897626"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="3bf9f-103">Функция Мактипетоаддресстипе</span><span class="sxs-lookup"><span data-stu-id="3bf9f-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="3bf9f-104">Функция **мактипетоаддресстипе** преобразует данный тип Mac в тип адреса.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bf9f-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="3bf9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bf9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf9f-107">*MacType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bf9f-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf9f-108">Преобразуемый тип MAC.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-108">MAC type to be converted.</span></span> <span data-ttu-id="3bf9f-109">Укажите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-109">Specify one of the following values:</span></span>

<span data-ttu-id="3bf9f-110">\_тип Mac \_ Ethernet Mac \_ Type \_ токенринг Mac \_ Type \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="3bf9f-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf9f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bf9f-111">Return value</span></span>

<span data-ttu-id="3bf9f-112">Если функция выполнена успешно, возвращаемое значение является одним из следующих типов адресов.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="3bf9f-113">\_тип адреса \_ Ethernet адрес \_ тип \_ токенринг адрес \_ тип \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="3bf9f-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="3bf9f-114">Если функция не выполнена, тип MAC неизвестен, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="3bf9f-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bf9f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bf9f-115">Remarks</span></span>

<span data-ttu-id="3bf9f-116">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **мактипетоаддресстипе** .</span><span class="sxs-lookup"><span data-stu-id="3bf9f-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf9f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3bf9f-117">Requirements</span></span>



| <span data-ttu-id="3bf9f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3bf9f-118">Requirement</span></span> | <span data-ttu-id="3bf9f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3bf9f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf9f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bf9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf9f-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bf9f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3bf9f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bf9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf9f-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bf9f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3bf9f-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3bf9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bf9f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bf9f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3bf9f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3bf9f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3bf9f-127"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bf9f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bf9f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3bf9f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bf9f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bf9f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




