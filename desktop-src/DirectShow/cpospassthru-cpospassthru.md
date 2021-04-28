---
description: Метод конструктора Кпоспасссру. Кпоспасссру.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Кпоспасссру. Кпоспасссру, конструктор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085602"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="42465-103">Кпоспасссру. Кпоспасссру, конструктор</span><span class="sxs-lookup"><span data-stu-id="42465-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="42465-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="42465-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42465-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42465-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="42465-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42465-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="42465-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="42465-108">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="42465-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="42465-109">Выделите этот параметр в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="42465-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="42465-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="42465-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="42465-111">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="42465-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="42465-112">Если объект является агрегатным, передайте указатель на интерфейс **IUnknown** объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="42465-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="42465-113">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="42465-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="42465-114">*фр*</span><span class="sxs-lookup"><span data-stu-id="42465-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="42465-115">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42465-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="42465-116">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="42465-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="42465-117">*ппин*</span><span class="sxs-lookup"><span data-stu-id="42465-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="42465-118">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) входного ПИН-кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="42465-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



