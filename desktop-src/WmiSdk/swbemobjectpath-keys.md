---
description: Свойство Keys объекта Свбемобжектпас представляет собой объект Свбемнамедвалуесет, содержащий привязки значений ключа. Это свойство доступно только для чтения.
ms.assetid: 1919403d-6dea-4d41-9bc7-a622a9c9c2c8
ms.tgt_platform: multiple
title: Свойство Свбемобжектпас. Keys (Адоктинт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Keys
- ISWbemObjectPath.Keys
- ISWbemObjectPath.get_Keys
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898ae7dac4a9c63273a8ff45a85b5bbb65aaa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080529"
---
# <a name="swbemobjectpathkeys-property"></a><span data-ttu-id="3d0ea-104">Свбемобжектпас. Keys, свойство</span><span class="sxs-lookup"><span data-stu-id="3d0ea-104">SWbemObjectPath.Keys property</span></span>

<span data-ttu-id="3d0ea-105">Свойство **Keys** объекта [**свбемобжектпас**](swbemobjectpath.md) представляет собой объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , содержащий привязки значений ключа.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-105">The **Keys** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span> <span data-ttu-id="3d0ea-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-106">This property is read-only.</span></span>

<span data-ttu-id="3d0ea-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3d0ea-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3d0ea-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0ea-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d0ea-109">Syntax</span></span>


```VB
SWbemObjectPath.Keys As Object
```



## <a name="property-value"></a><span data-ttu-id="3d0ea-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3d0ea-110">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d0ea-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3d0ea-111">Error codes</span></span>

<span data-ttu-id="3d0ea-112">После получения свойства **Keys** объект **Err** может содержать приведенный ниже код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-112">After you retrieve the **Keys** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="3d0ea-113">**вбемеррнотсуппортед** -2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="3d0ea-113">**wbemErrNotSupported** - 2147749900 (0x8004100C)</span></span>
</dt> <dd>

<span data-ttu-id="3d0ea-114">Эта функция или операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-114">The feature or operation is not supported.</span></span> <span data-ttu-id="3d0ea-115">Эта ошибка возвращается, если скрипт пытается выполнить запись в это свойство.</span><span class="sxs-lookup"><span data-stu-id="3d0ea-115">This error is returned if a script attempts to write to this property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d0ea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3d0ea-116">Requirements</span></span>



| <span data-ttu-id="3d0ea-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3d0ea-117">Requirement</span></span> | <span data-ttu-id="3d0ea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3d0ea-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0ea-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d0ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d0ea-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d0ea-120">Windows Vista</span></span><br/>                                                                                   |
| <span data-ttu-id="3d0ea-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d0ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d0ea-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d0ea-122">Windows Server 2008</span></span><br/>                                                                             |
| <span data-ttu-id="3d0ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="3d0ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d0ea-124"><dt>Адоктинт. h (включение Wbemdisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d0ea-124"><dt>Adoctint.h (include Wbemdisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="3d0ea-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3d0ea-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d0ea-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d0ea-126"><dt>Wbemdisp.tlb</dt></span></span> </dl>                    |
| <span data-ttu-id="3d0ea-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3d0ea-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d0ea-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d0ea-128"><dt>Wbemdisp.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="3d0ea-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="3d0ea-129">CLSID</span></span><br/>                    | <span data-ttu-id="3d0ea-130">\_СВБЕМОБЖЕКТПАС CLSID</span><span class="sxs-lookup"><span data-stu-id="3d0ea-130">CLSID\_SWbemObjectPath</span></span><br/>                                                                          |
| <span data-ttu-id="3d0ea-131">IID</span><span class="sxs-lookup"><span data-stu-id="3d0ea-131">IID</span></span><br/>                      | <span data-ttu-id="3d0ea-132">IID \_ исвбемобжектпас</span><span class="sxs-lookup"><span data-stu-id="3d0ea-132">IID\_ISWbemObjectPath</span></span><br/>                                                                           |



 

 




