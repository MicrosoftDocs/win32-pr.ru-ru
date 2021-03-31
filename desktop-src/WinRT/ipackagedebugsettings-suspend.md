---
description: Приостанавливает процессы пакета, если они выполняются в данный момент.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Метод Ипаккажедебугсеттингс:: Suspend'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809772"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="dc611-103">Метод Ипаккажедебугсеттингс:: Suspend</span><span class="sxs-lookup"><span data-stu-id="dc611-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="dc611-104">Приостанавливает процессы пакета, если они выполняются в данный момент.</span><span class="sxs-lookup"><span data-stu-id="dc611-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc611-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc611-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="dc611-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc611-107">*полноеимяпакета* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc611-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc611-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="dc611-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="dc611-109">Полное имя пакета.</span><span class="sxs-lookup"><span data-stu-id="dc611-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc611-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc611-110">Return value</span></span>

<span data-ttu-id="dc611-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc611-111">Type: **HRESULT**</span></span>

<span data-ttu-id="dc611-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dc611-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dc611-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc611-113">Return code</span></span>                                                                                            | <span data-ttu-id="dc611-114">Описание</span><span class="sxs-lookup"><span data-stu-id="dc611-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="dc611-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="dc611-116">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="dc611-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="dc611-117"><dt>**E \_ недопустимое \_ STATECHANGE**</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="dc611-118">Процесс в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc611-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc611-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc611-119">Remarks</span></span>

<span data-ttu-id="dc611-120">Каждый процесс получает событие [**приостановки**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="dc611-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="dc611-121">Он может быть полезен разработчикам для пошагового указания того, как приложения реагируют на это событие.</span><span class="sxs-lookup"><span data-stu-id="dc611-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc611-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dc611-122">Requirements</span></span>



| <span data-ttu-id="dc611-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dc611-123">Requirement</span></span> | <span data-ttu-id="dc611-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dc611-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc611-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc611-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dc611-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dc611-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="dc611-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc611-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dc611-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc611-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="dc611-129">IDL</span><span class="sxs-lookup"><span data-stu-id="dc611-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc611-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc611-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc611-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc611-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc611-132">[**ипаккажедебугсеттингс**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dc611-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
