---
description: Проверяет существование всех временных подписчиков в хранилище данных. Вызывая этот метод, можно убедиться, что все временные подписчики, перечисленные в хранилище данных, активны.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Метод IEventSystem2:: Верифитрансиентсубскриберс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990507"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a><span data-ttu-id="68aef-104">Метод IEventSystem2:: Верифитрансиентсубскриберс</span><span class="sxs-lookup"><span data-stu-id="68aef-104">IEventSystem2::VerifyTransientSubscribers method</span></span>

<span data-ttu-id="68aef-105">Проверяет существование всех временных подписчиков в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="68aef-105">Verifies the existence of all transient subscribers in the data store.</span></span> <span data-ttu-id="68aef-106">Вызывая этот метод, можно убедиться, что все временные подписчики, перечисленные в хранилище данных, активны.</span><span class="sxs-lookup"><span data-stu-id="68aef-106">By calling this method, you can ensure that all transient subscribers listed in the data store are active.</span></span>

## <a name="syntax"></a><span data-ttu-id="68aef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68aef-107">Syntax</span></span>


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a><span data-ttu-id="68aef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68aef-108">Parameters</span></span>

<span data-ttu-id="68aef-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="68aef-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68aef-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68aef-110">Return value</span></span>

<span data-ttu-id="68aef-111">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="68aef-111">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="68aef-112">Требования</span><span class="sxs-lookup"><span data-stu-id="68aef-112">Requirements</span></span>



| <span data-ttu-id="68aef-113">Требование</span><span class="sxs-lookup"><span data-stu-id="68aef-113">Requirement</span></span> | <span data-ttu-id="68aef-114">Значение</span><span class="sxs-lookup"><span data-stu-id="68aef-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="68aef-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68aef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="68aef-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aef-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="68aef-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68aef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="68aef-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aef-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="68aef-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68aef-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68aef-120">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="68aef-120">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




