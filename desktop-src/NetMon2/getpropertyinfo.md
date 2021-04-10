---
description: Функция GetPropertyInfo возвращает указатель на сведения о свойстве данного протокола.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Функция GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896774"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="48768-103">Функция GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="48768-103">GetPropertyInfo function</span></span>

<span data-ttu-id="48768-104">Функция **GetPropertyInfo** возвращает указатель на сведения о свойстве данного протокола.</span><span class="sxs-lookup"><span data-stu-id="48768-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="48768-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48768-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="48768-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48768-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48768-107">*хпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48768-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48768-108">Обработчик для свойства.</span><span class="sxs-lookup"><span data-stu-id="48768-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48768-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48768-109">Return value</span></span>

<span data-ttu-id="48768-110">Если функция выполнена успешно, возвращаемое значение является указателем на свойство.</span><span class="sxs-lookup"><span data-stu-id="48768-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="48768-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="48768-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="48768-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48768-112">Remarks</span></span>

<span data-ttu-id="48768-113">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **GetPropertyInfo** .</span><span class="sxs-lookup"><span data-stu-id="48768-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="48768-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48768-114">Requirements</span></span>



| <span data-ttu-id="48768-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48768-115">Requirement</span></span> | <span data-ttu-id="48768-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48768-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48768-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48768-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48768-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48768-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="48768-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48768-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48768-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48768-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="48768-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="48768-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48768-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="48768-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="48768-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48768-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="48768-124"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48768-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="48768-125">DLL</span><span class="sxs-lookup"><span data-stu-id="48768-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48768-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48768-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




