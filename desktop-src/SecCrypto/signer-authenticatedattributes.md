---
description: Извлекает коллекцию атрибутов, прошедших проверку подлинности.
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: Свойство SignIn. Аусентикатедаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685172"
---
# <a name="signerauthenticatedattributes-property"></a><span data-ttu-id="bf321-103">Свойство SignIn. Аусентикатедаттрибутес</span><span class="sxs-lookup"><span data-stu-id="bf321-103">Signer.AuthenticatedAttributes property</span></span>

<span data-ttu-id="bf321-104">\[Свойство **аусентикатедаттрибутес** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bf321-104">\[The **AuthenticatedAttributes** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bf321-105">Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="bf321-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bf321-106">Свойство **аусентикатедаттрибутес** извлекает коллекцию атрибутов, прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="bf321-106">The **AuthenticatedAttributes** property retrieves the collection of authenticated attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf321-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf321-107">Syntax</span></span>


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a><span data-ttu-id="bf321-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bf321-108">Property value</span></span>

<span data-ttu-id="bf321-109">Коллекция [**Attributes**](attributes.md) , представляющая атрибуты, прошедшие проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="bf321-109">An [**Attributes**](attributes.md) collection that represents the signer's authenticated attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf321-110">Требования</span><span class="sxs-lookup"><span data-stu-id="bf321-110">Requirements</span></span>



| <span data-ttu-id="bf321-111">Требование</span><span class="sxs-lookup"><span data-stu-id="bf321-111">Requirement</span></span> | <span data-ttu-id="bf321-112">Значение</span><span class="sxs-lookup"><span data-stu-id="bf321-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf321-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bf321-113">Redistributable</span></span><br/> | <span data-ttu-id="bf321-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf321-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bf321-115">DLL</span><span class="sxs-lookup"><span data-stu-id="bf321-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bf321-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf321-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf321-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf321-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf321-118">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="bf321-118">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
