---
description: Возвращает номер версии системы событий.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'Метод IEventSystem2:: метода Version'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496656"
---
# <a name="ieventsystem2getversion-method"></a><span data-ttu-id="37139-103">Метод IEventSystem2:: метода Version</span><span class="sxs-lookup"><span data-stu-id="37139-103">IEventSystem2::GetVersion method</span></span>

<span data-ttu-id="37139-104">Возвращает номер версии системы событий.</span><span class="sxs-lookup"><span data-stu-id="37139-104">Retrieves the version number of the event system.</span></span>

## <a name="syntax"></a><span data-ttu-id="37139-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37139-105">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a><span data-ttu-id="37139-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37139-107">*пнверсион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="37139-107">*pnVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37139-108">Номер версии системы событий.</span><span class="sxs-lookup"><span data-stu-id="37139-108">The version number of the event system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37139-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37139-109">Return value</span></span>

<span data-ttu-id="37139-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="37139-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="37139-111">Требования</span><span class="sxs-lookup"><span data-stu-id="37139-111">Requirements</span></span>



| <span data-ttu-id="37139-112">Требование</span><span class="sxs-lookup"><span data-stu-id="37139-112">Requirement</span></span> | <span data-ttu-id="37139-113">Значение</span><span class="sxs-lookup"><span data-stu-id="37139-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="37139-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37139-114">Minimum supported client</span></span><br/> | <span data-ttu-id="37139-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37139-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="37139-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37139-116">Minimum supported server</span></span><br/> | <span data-ttu-id="37139-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="37139-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="37139-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37139-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37139-119">**IEventSystem2**</span><span class="sxs-lookup"><span data-stu-id="37139-119">**IEventSystem2**</span></span>](ieventsystem2.md)
</dt> </dl>

 

 




