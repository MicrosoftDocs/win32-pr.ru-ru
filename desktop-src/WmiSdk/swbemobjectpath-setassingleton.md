---
description: Метод Сетассинглетон объекта Свбемобжектпас заставляет путь обращаться к единственному экземпляру WMI класса. Одноэлементный класс — это класс, который не может иметь более одного экземпляра.
ms.assetid: 7ec53954-2aac-494c-87c7-6a14592d8bd5
ms.tgt_platform: multiple
title: Свбемобжектпас. Сетассинглетон, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
- ISWbemObjectPath.SetAsSingleton
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5335f595eccc996ece9f941092ffffae487352fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712935"
---
# <a name="swbemobjectpathsetassingleton-method"></a><span data-ttu-id="2cb29-104">Свбемобжектпас. Сетассинглетон, метод</span><span class="sxs-lookup"><span data-stu-id="2cb29-104">SWbemObjectPath.SetAsSingleton method</span></span>

<span data-ttu-id="2cb29-105">Метод **сетассинглетон** объекта [**свбемобжектпас**](swbemobjectpath.md) заставляет путь обращаться к единственному экземпляру WMI класса.</span><span class="sxs-lookup"><span data-stu-id="2cb29-105">The **SetAsSingleton** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a singleton WMI instance of a class.</span></span> <span data-ttu-id="2cb29-106">Одноэлементный класс — это класс, который не может иметь более одного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2cb29-106">A singleton class is a class that can never have more than one instance.</span></span>

<span data-ttu-id="2cb29-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2cb29-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span> <span data-ttu-id="2cb29-108">свбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="2cb29-108">SWbemObjectPath</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb29-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cb29-109">Syntax</span></span>


```VB
SWbemObjectPath.SetAsSingleton()
```



## <a name="parameters"></a><span data-ttu-id="2cb29-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cb29-110">Parameters</span></span>

<span data-ttu-id="2cb29-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2cb29-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cb29-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cb29-112">Return value</span></span>

<span data-ttu-id="2cb29-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2cb29-113">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2cb29-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2cb29-114">Error codes</span></span>

<span data-ttu-id="2cb29-115">После завершения метода **сетассинглетон** объект **Err** может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2cb29-115">Upon completion of the **SetAsSingleton** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="2cb29-116">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2cb29-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2cb29-117">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2cb29-117">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cb29-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2cb29-118">Requirements</span></span>



| <span data-ttu-id="2cb29-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2cb29-119">Requirement</span></span> | <span data-ttu-id="2cb29-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2cb29-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb29-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2cb29-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb29-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cb29-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2cb29-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2cb29-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb29-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cb29-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2cb29-125">Header</span><span class="sxs-lookup"><span data-stu-id="2cb29-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cb29-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb29-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cb29-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2cb29-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cb29-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2cb29-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2cb29-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb29-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb29-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb29-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cb29-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="2cb29-131">CLSID</span></span><br/>                    | <span data-ttu-id="2cb29-132">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="2cb29-132">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="2cb29-133">IID</span><span class="sxs-lookup"><span data-stu-id="2cb29-133">IID</span></span><br/>                      | <span data-ttu-id="2cb29-134">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="2cb29-134">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




