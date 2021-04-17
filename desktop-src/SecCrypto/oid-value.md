---
description: Задает или получает значение кода OID с точкой в идентификаторе.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: Кода. Value, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669457"
---
# <a name="oidvalue-property"></a><span data-ttu-id="8d30f-103">Кода. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="8d30f-103">OID.Value property</span></span>

<span data-ttu-id="8d30f-104">\[Свойство **value** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8d30f-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d30f-105">Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="8d30f-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8d30f-106">Свойство **value** задает или получает значение кода OID с точками идентификатора.</span><span class="sxs-lookup"><span data-stu-id="8d30f-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d30f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d30f-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="8d30f-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8d30f-108">Property value</span></span>

<span data-ttu-id="8d30f-109">Значение кода OID с точками идентификатора.</span><span class="sxs-lookup"><span data-stu-id="8d30f-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="8d30f-110">Возможные значения см. в разделе Винкрипт. h.</span><span class="sxs-lookup"><span data-stu-id="8d30f-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d30f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d30f-111">Remarks</span></span>

<span data-ttu-id="8d30f-112">Если задано свойство **value** , для свойства [**FriendlyName**](oid-friendlyname.md) задается соответствующее отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="8d30f-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="8d30f-113">Если задано свойство **FriendlyName** , свойству **value** присваивается соответствующее значение с точками.</span><span class="sxs-lookup"><span data-stu-id="8d30f-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d30f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8d30f-114">Requirements</span></span>



| <span data-ttu-id="8d30f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8d30f-115">Requirement</span></span> | <span data-ttu-id="8d30f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30f-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d30f-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8d30f-117">Redistributable</span></span><br/> | <span data-ttu-id="8d30f-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d30f-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d30f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8d30f-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d30f-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d30f-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d30f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d30f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d30f-122">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="8d30f-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
