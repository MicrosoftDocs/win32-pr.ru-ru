---
description: Получает логическое значение, указывающее, имеется ли расширение Кэйусаже.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Кэйусаже. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665029"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="47239-103">Кэйусаже. Present, свойство</span><span class="sxs-lookup"><span data-stu-id="47239-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="47239-104">\[Свойство **Present** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="47239-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="47239-105">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="47239-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="47239-106">Свойство **Present** получает логическое значение, указывающее, имеется ли расширение [**кэйусаже**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="47239-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="47239-107">Это свойство является свойством по умолчанию объекта [**кэйусаже**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="47239-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="47239-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47239-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="47239-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="47239-109">Property value</span></span>

<span data-ttu-id="47239-110">Если задано **значение true**, используется расширение кэйусаже.</span><span class="sxs-lookup"><span data-stu-id="47239-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="47239-111">Требования</span><span class="sxs-lookup"><span data-stu-id="47239-111">Requirements</span></span>



| <span data-ttu-id="47239-112">Требование</span><span class="sxs-lookup"><span data-stu-id="47239-112">Requirement</span></span> | <span data-ttu-id="47239-113">Значение</span><span class="sxs-lookup"><span data-stu-id="47239-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47239-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="47239-114">Redistributable</span></span><br/> | <span data-ttu-id="47239-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="47239-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="47239-116">DLL</span><span class="sxs-lookup"><span data-stu-id="47239-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="47239-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47239-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47239-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47239-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47239-119">**кэйусаже**</span><span class="sxs-lookup"><span data-stu-id="47239-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
