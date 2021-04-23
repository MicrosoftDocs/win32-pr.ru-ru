---
description: Метод Сетаскласс объекта Свбемобжектпас заставляет путь обращаться к классу WMI.
ms.assetid: d341b980-bac9-4db4-a55f-eb971fb385da
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. Сетаскласс (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.SetAsClass
- ISWbemObjectPath.SetAsClass
- ISWbemObjectPath.put_SetAsClass
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 371fe95c3a7152767c45849191658c4bcb661750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711635"
---
# <a name="swbemobjectpathsetasclass-property"></a><span data-ttu-id="b1594-103">Свбемобжектпас. Сетаскласс, свойство</span><span class="sxs-lookup"><span data-stu-id="b1594-103">SWbemObjectPath.SetAsClass property</span></span>

<span data-ttu-id="b1594-104">Метод **сетаскласс** объекта [**свбемобжектпас**](swbemobjectpath.md) заставляет путь обращаться к классу WMI.</span><span class="sxs-lookup"><span data-stu-id="b1594-104">The **SetAsClass** method of the [**SWbemObjectPath**](swbemobjectpath.md) object forces the path to address a WMI class.</span></span>

<span data-ttu-id="b1594-105">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="b1594-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1594-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1594-106">Syntax</span></span>


```VB
SWbemObjectPath.SetAsClass
```



## <a name="property-value"></a><span data-ttu-id="b1594-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b1594-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1594-108">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b1594-108">Error codes</span></span>

<span data-ttu-id="b1594-109">После получения или задания свойства **сетаскласс** объект **Err** может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1594-109">After you get or set the **SetAsClass** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="b1594-110">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b1594-110">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b1594-111">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1594-111">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1594-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b1594-112">Requirements</span></span>



| <span data-ttu-id="b1594-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b1594-113">Requirement</span></span> | <span data-ttu-id="b1594-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b1594-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1594-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1594-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b1594-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1594-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1594-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1594-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b1594-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1594-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1594-119">Header</span><span class="sxs-lookup"><span data-stu-id="b1594-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1594-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1594-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1594-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b1594-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1594-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1594-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1594-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b1594-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1594-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1594-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1594-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1594-125">CLSID</span></span><br/>                    | <span data-ttu-id="b1594-126">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="b1594-126">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="b1594-127">IID</span><span class="sxs-lookup"><span data-stu-id="b1594-127">IID</span></span><br/>                      | <span data-ttu-id="b1594-128">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="b1594-128">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




