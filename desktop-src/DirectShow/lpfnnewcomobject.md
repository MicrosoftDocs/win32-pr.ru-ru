---
description: Указатель на функцию, которая создает экземпляр объекта.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Указатель функции Лпфнневкомобжект (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689075"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="e144b-103">Указатель функции Лпфнневкомобжект</span><span class="sxs-lookup"><span data-stu-id="e144b-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="e144b-104">Указатель на функцию, которая создает экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="e144b-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e144b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e144b-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e144b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e144b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e144b-107">*пункаутер*</span><span class="sxs-lookup"><span data-stu-id="e144b-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="e144b-108">Указатель на интерфейс **IUnknown** объекта, который выполняет статистическую обработку нового объекта, если он имеется.</span><span class="sxs-lookup"><span data-stu-id="e144b-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="e144b-109">Этот указатель может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e144b-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e144b-110">*фр*</span><span class="sxs-lookup"><span data-stu-id="e144b-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e144b-111">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e144b-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="e144b-112">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e144b-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e144b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e144b-113">Return value</span></span>

<span data-ttu-id="e144b-114">Возвращает указатель на новый экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="e144b-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e144b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e144b-115">Requirements</span></span>



| <span data-ttu-id="e144b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e144b-116">Requirement</span></span> | <span data-ttu-id="e144b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e144b-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e144b-118">Header</span><span class="sxs-lookup"><span data-stu-id="e144b-118">Header</span></span><br/> | <dl> <span data-ttu-id="e144b-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e144b-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e144b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e144b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e144b-121">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="e144b-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




