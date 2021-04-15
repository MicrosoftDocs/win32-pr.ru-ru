---
description: Функция Финдпропертинстанце находит первый экземпляр свойства, указанного параметром Хпроперти.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Функция Финдпропертинстанце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662195"
---
# <a name="findpropertyinstance-function"></a><span data-ttu-id="f3f20-103">Функция Финдпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="f3f20-103">FindPropertyInstance function</span></span>

<span data-ttu-id="f3f20-104">Функция **финдпропертинстанце** находит первый экземпляр свойства, указанного параметром *хпроперти* .</span><span class="sxs-lookup"><span data-stu-id="f3f20-104">The **FindPropertyInstance** function finds the first instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3f20-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="f3f20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3f20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f20-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3f20-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f20-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="f3f20-108">Handle to the frame.</span></span> <span data-ttu-id="f3f20-109">Маркер кадра можно извлечь с помощью вызова функции [noframes](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f20-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3f20-110">*хпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3f20-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f20-111">Обработчик для свойства, которое необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="f3f20-111">Handle to the property you want to find.</span></span> <span data-ttu-id="f3f20-112">Маркер свойства может быть получен путем вызова функции- [Свойства](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f20-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f20-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3f20-113">Return value</span></span>

<span data-ttu-id="f3f20-114">Если функция выполнена успешно (то есть, если свойство найдено), возвращаемое значение является указателем на первый экземпляр свойства.</span><span class="sxs-lookup"><span data-stu-id="f3f20-114">If the function is successful (that is, if the property is found), the return value is a pointer to the first instance of the property.</span></span>

<span data-ttu-id="f3f20-115">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f3f20-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f20-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3f20-116">Remarks</span></span>

<span data-ttu-id="f3f20-117">Чтобы получить следующий экземпляр свойства, вызовите [финдпропертинстанцерестарт](findpropertyinstancerestart.md).</span><span class="sxs-lookup"><span data-stu-id="f3f20-117">To retrieve the next instance of the property, call [FindPropertyInstanceRestart](findpropertyinstancerestart.md).</span></span>

<span data-ttu-id="f3f20-118">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md)могут вызывать функцию **финдпропертинстанце** .</span><span class="sxs-lookup"><span data-stu-id="f3f20-118">[*Experts*](e.md) and [*parsers*](p.md)can call the **FindPropertyInstance** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f20-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f3f20-119">Requirements</span></span>



| <span data-ttu-id="f3f20-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f3f20-120">Requirement</span></span> | <span data-ttu-id="f3f20-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3f20-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f20-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3f20-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f20-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3f20-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f3f20-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3f20-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f20-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f3f20-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3f20-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f3f20-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f20-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f20-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f3f20-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f3f20-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3f20-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3f20-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f3f20-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f20-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f20-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f20-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3f20-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3f20-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f20-133">финдпропертинстанцерестарт</span><span class="sxs-lookup"><span data-stu-id="f3f20-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




