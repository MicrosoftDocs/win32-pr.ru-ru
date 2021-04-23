---
description: Находит следующий экземпляр свойства, указанного параметром Хпроперти.
ms.assetid: f77cb92b-5936-4349-bf66-643c16e9e0df
title: Функция Финдпропертинстанцерестарт (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstanceRestart
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d1e731bb00b28bb62862dd18fbd6031fa973fe38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662194"
---
# <a name="findpropertyinstancerestart-function"></a><span data-ttu-id="ff6da-103">Функция Финдпропертинстанцерестарт</span><span class="sxs-lookup"><span data-stu-id="ff6da-103">FindPropertyInstanceRestart function</span></span>

<span data-ttu-id="ff6da-104">Функция **финдпропертинстанцерестарт** находит следующий экземпляр свойства, указанного параметром *хпроперти* .</span><span class="sxs-lookup"><span data-stu-id="ff6da-104">The **FindPropertyInstanceRestart** function finds the next instance of the property specified by the *hProperty* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff6da-105">Syntax</span></span>


```C++
LPPROPERTYINST WINAPI FindPropertyInstanceRestart(
  _In_ HFRAME         hFrame,
  _In_ HPROPERTY      hProperty,
  _In_ LPPROPERTYINST *lpRestartKey,
  _In_ BOOL           DirForward
);
```



## <a name="parameters"></a><span data-ttu-id="ff6da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff6da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff6da-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6da-108">Маркер фрейма.</span><span class="sxs-lookup"><span data-stu-id="ff6da-108">A handle to the frame.</span></span> <span data-ttu-id="ff6da-109">Маркер кадра можно извлечь с помощью вызова функции [noframes](getframe.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6da-109">The frame handle can be retrieved by a call to the [GetFrame](getframe.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ff6da-110">*хпроперти* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-110">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6da-111">Описатель искомого свойства.</span><span class="sxs-lookup"><span data-stu-id="ff6da-111">A handle to the property to find.</span></span> <span data-ttu-id="ff6da-112">Маркер свойства может быть получен путем вызова функции- [Свойства](getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6da-112">The property handle can be retrieved by a call to the [GetProperty](getproperty.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ff6da-113">*лпрестарткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-113">*lpRestartKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6da-114">Указатель на экземпляр свойства, используемый в качестве начальной точки поиска.</span><span class="sxs-lookup"><span data-stu-id="ff6da-114">A pointer to the property instance used as the starting point of the search.</span></span> <span data-ttu-id="ff6da-115">Если параметр *лпрестарткэй* имеет значение **null**, поиск начинается в начале кадра или в конце кадра в зависимости от значения параметра *дирфорвард* .</span><span class="sxs-lookup"><span data-stu-id="ff6da-115">If the *lpRestartKey* parameter is set to **NULL**, the search begins at beginning of the frame, or the end of the frame, depending on the value of the *DirForward* parameter.</span></span>

<span data-ttu-id="ff6da-116">Если *лпрестарткэй* указывает на **null**, поиск начинается в начале кадра, если *дирфорвард* имеет **значение true** , или в конце кадра, если параметр имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ff6da-116">If *lpRestartKey* points to **NULL**, the search begins at the beginning of the frame if *DirForward* is **TRUE** or the at end of the frame if the parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ff6da-117">*Дирфорвард* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-117">*DirForward* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6da-118">Индикатор направления поиска.</span><span class="sxs-lookup"><span data-stu-id="ff6da-118">An indicator of the search direction.</span></span> <span data-ttu-id="ff6da-119">Если значение равно **true**, Поиск перемещается от текущего положения к концу кадра.</span><span class="sxs-lookup"><span data-stu-id="ff6da-119">If the value is **TRUE**, the search moves from the current location to the end of the frame.</span></span> <span data-ttu-id="ff6da-120">Если значение равно **false**, Поиск перемещается от текущего положения к началу кадра.</span><span class="sxs-lookup"><span data-stu-id="ff6da-120">If the value is **FALSE**, the search moves from the current location to the beginning of the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff6da-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff6da-121">Return value</span></span>

<span data-ttu-id="ff6da-122">Если функция выполнена успешно, возвращаемое значение будет следующим допустимым **лппропертинст**.</span><span class="sxs-lookup"><span data-stu-id="ff6da-122">If the function is successful, the return value is the next valid **LPPROPERTYINST**.</span></span>

<span data-ttu-id="ff6da-123">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ff6da-123">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff6da-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff6da-124">Remarks</span></span>

<span data-ttu-id="ff6da-125">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **финдпропертинстанцерестарт** .</span><span class="sxs-lookup"><span data-stu-id="ff6da-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **FindPropertyInstanceRestart** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6da-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ff6da-126">Requirements</span></span>



| <span data-ttu-id="ff6da-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ff6da-127">Requirement</span></span> | <span data-ttu-id="ff6da-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ff6da-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6da-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff6da-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff6da-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff6da-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff6da-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff6da-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff6da-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff6da-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff6da-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff6da-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff6da-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ff6da-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff6da-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff6da-136"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff6da-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff6da-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ff6da-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff6da-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff6da-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff6da-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff6da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6da-140">GetFrame</span><span class="sxs-lookup"><span data-stu-id="ff6da-140">GetFrame</span></span>](getframe.md)
</dt> <dt>

[<span data-ttu-id="ff6da-141">GetProperty</span><span class="sxs-lookup"><span data-stu-id="ff6da-141">GetProperty</span></span>](getproperty.md)
</dt> </dl>

 

 




