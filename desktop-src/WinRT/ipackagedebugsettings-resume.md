---
description: Возобновляет процессы пакета, если они в данный момент приостановлены.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Метод Ипаккажедебугсеттингс:: Resume'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711058"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="33281-103">Метод Ипаккажедебугсеттингс:: Resume</span><span class="sxs-lookup"><span data-stu-id="33281-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="33281-104">Возобновляет процессы пакета, если они в данный момент приостановлены.</span><span class="sxs-lookup"><span data-stu-id="33281-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="33281-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33281-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="33281-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33281-107">*полноеимяпакета* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33281-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33281-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="33281-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="33281-109">Полное имя пакета.</span><span class="sxs-lookup"><span data-stu-id="33281-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33281-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33281-110">Return value</span></span>

<span data-ttu-id="33281-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="33281-111">Type: **HRESULT**</span></span>

<span data-ttu-id="33281-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="33281-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33281-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33281-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33281-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33281-114">Remarks</span></span>

<span data-ttu-id="33281-115">Каждый процесс получает событие [**возобновления**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="33281-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="33281-116">Он может быть полезен разработчикам для пошагового указания того, как приложения реагируют на это событие.</span><span class="sxs-lookup"><span data-stu-id="33281-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="33281-117">Требования</span><span class="sxs-lookup"><span data-stu-id="33281-117">Requirements</span></span>



| <span data-ttu-id="33281-118">Требование</span><span class="sxs-lookup"><span data-stu-id="33281-118">Requirement</span></span> | <span data-ttu-id="33281-119">Значение</span><span class="sxs-lookup"><span data-stu-id="33281-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33281-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33281-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33281-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="33281-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="33281-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33281-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33281-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33281-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="33281-124">IDL</span><span class="sxs-lookup"><span data-stu-id="33281-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33281-125"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33281-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33281-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33281-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="33281-127">[**ипаккажедебугсеттингс**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33281-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
