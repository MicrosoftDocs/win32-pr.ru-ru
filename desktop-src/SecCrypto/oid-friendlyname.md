---
description: Задает или получает отображаемое имя для идентификатора.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: Кода. FriendlyName, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669166"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="cc041-103">Кода. FriendlyName, свойство</span><span class="sxs-lookup"><span data-stu-id="cc041-103">OID.FriendlyName property</span></span>

<span data-ttu-id="cc041-104">\[Свойство **FriendlyName** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cc041-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cc041-105">Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cc041-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cc041-106">Свойство **FriendlyName** задает или получает отображаемое имя для идентификатора.</span><span class="sxs-lookup"><span data-stu-id="cc041-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc041-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc041-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="cc041-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cc041-108">Property value</span></span>

<span data-ttu-id="cc041-109">Отображаемое имя [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="cc041-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc041-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc041-110">Remarks</span></span>

<span data-ttu-id="cc041-111">Если задано свойство **FriendlyName** , свойству [**value**](oid-value.md) присваивается соответствующее значение с точками.</span><span class="sxs-lookup"><span data-stu-id="cc041-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="cc041-112">Если задано свойство **value** , для свойства **FriendlyName** задается соответствующее отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="cc041-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc041-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cc041-113">Requirements</span></span>



| <span data-ttu-id="cc041-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cc041-114">Requirement</span></span> | <span data-ttu-id="cc041-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cc041-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc041-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cc041-116">Redistributable</span></span><br/> | <span data-ttu-id="cc041-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc041-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cc041-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cc041-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="cc041-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc041-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc041-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc041-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc041-121">**КОДА**</span><span class="sxs-lookup"><span data-stu-id="cc041-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
