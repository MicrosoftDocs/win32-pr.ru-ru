---
description: Функция-свойство возвращает маркер для заданного свойства.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Функция Property (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990898"
---
# <a name="getproperty-function"></a><span data-ttu-id="2b4e3-103">Функция Property</span><span class="sxs-lookup"><span data-stu-id="2b4e3-103">GetProperty function</span></span>

<span data-ttu-id="2b4e3-104">Функция- **свойство** возвращает маркер для заданного свойства.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b4e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b4e3-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="2b4e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b4e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b4e3-107">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b4e3-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4e3-108">Обработчик для протокола.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="2b4e3-109">*PropertyName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b4e3-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b4e3-110">Имя свойства (например, **CHECKSUM**).</span><span class="sxs-lookup"><span data-stu-id="2b4e3-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b4e3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b4e3-111">Return value</span></span>

<span data-ttu-id="2b4e3-112">Если функция выполнена успешно, возвращаемое значение является маркером свойства.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="2b4e3-113">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b4e3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b4e3-114">Remarks</span></span>

<span data-ttu-id="2b4e3-115">Функцию **Property** можно использовать для получения маркера свойства, необходимого для размещения экземпляров свойства.</span><span class="sxs-lookup"><span data-stu-id="2b4e3-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="2b4e3-116">Функции, используемые для размещения экземпляров свойств, — это [финдпропертинстанце](findpropertyinstance.md) (который находит первый экземпляр) и [финдпропертинстанцерестарт](findpropertyinstancerestart.md) (который находит следующий экземпляр).</span><span class="sxs-lookup"><span data-stu-id="2b4e3-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="2b4e3-117">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **Property** .</span><span class="sxs-lookup"><span data-stu-id="2b4e3-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b4e3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2b4e3-118">Requirements</span></span>



| <span data-ttu-id="2b4e3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2b4e3-119">Requirement</span></span> | <span data-ttu-id="2b4e3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2b4e3-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b4e3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b4e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b4e3-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b4e3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2b4e3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b4e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b4e3-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b4e3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2b4e3-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b4e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b4e3-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b4e3-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2b4e3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b4e3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b4e3-128"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b4e3-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b4e3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2b4e3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b4e3-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b4e3-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b4e3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b4e3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4e3-132">финдпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="2b4e3-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="2b4e3-133">финдпропертинстанцерестарт</span><span class="sxs-lookup"><span data-stu-id="2b4e3-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




