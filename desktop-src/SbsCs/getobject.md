---
description: Метод GetObject возвращает экземпляр существующего объекта Microsoft. Windows. Акткткс.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: Акткткс. GetObject, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809371"
---
# <a name="actctxgetobject-method"></a><span data-ttu-id="7888c-103">Акткткс. GetObject, метод</span><span class="sxs-lookup"><span data-stu-id="7888c-103">ActCtx.GetObject method</span></span>

<span data-ttu-id="7888c-104">Метод **GetObject** возвращает экземпляр существующего объекта [**Microsoft. Windows. акткткс**](microsoft-windows-actctx-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7888c-104">The **GetObject** method gets an instance of an existing [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7888c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7888c-105">Syntax</span></span>


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a><span data-ttu-id="7888c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7888c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7888c-107">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="7888c-107">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="7888c-108">Обязательная строка, указывающая на объект.</span><span class="sxs-lookup"><span data-stu-id="7888c-108">Required string that indicates the object.</span></span> <span data-ttu-id="7888c-109">Имя должно быть в реестре в разделе **hKey \_ локальный \_ компьютер** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation**.</span><span class="sxs-lookup"><span data-stu-id="7888c-109">The name must be in the registry under **HKEY\_LOCAL\_MACHINE**\\**Microsoft**\\**Visual Studio**\\**6.0**\\**<package>**\\**Automation**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7888c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7888c-110">Return value</span></span>

<span data-ttu-id="7888c-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7888c-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7888c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7888c-112">Requirements</span></span>



| <span data-ttu-id="7888c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7888c-113">Requirement</span></span> | <span data-ttu-id="7888c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7888c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7888c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7888c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7888c-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7888c-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7888c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7888c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7888c-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7888c-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7888c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7888c-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7888c-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7888c-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="7888c-121">IID</span><span class="sxs-lookup"><span data-stu-id="7888c-121">IID</span></span><br/>                      | <span data-ttu-id="7888c-122">IID \_ иакткткс определен как 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="7888c-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7888c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7888c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7888c-124">**Метод CreateObject**</span><span class="sxs-lookup"><span data-stu-id="7888c-124">**CreateObject Method**</span></span>](createobject.md)
</dt> </dl>

 

 




