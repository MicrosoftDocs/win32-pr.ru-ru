---
description: Извлекает коллекцию номеров пользовательских уведомлений.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Свойство квалификатора. Нотиценумберс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648792"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="abe79-103">Свойство квалификатора. Нотиценумберс</span><span class="sxs-lookup"><span data-stu-id="abe79-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="abe79-104">\[Свойство **нотиценумберс** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="abe79-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="abe79-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="abe79-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="abe79-106">Свойство **нотиценумберс** извлекает коллекцию номеров пользовательских уведомлений.</span><span class="sxs-lookup"><span data-stu-id="abe79-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="abe79-107">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="abe79-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe79-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abe79-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="abe79-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="abe79-109">Property value</span></span>

<span data-ttu-id="abe79-110">Коллекция номеров пользовательских уведомлений.</span><span class="sxs-lookup"><span data-stu-id="abe79-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe79-111">Требования</span><span class="sxs-lookup"><span data-stu-id="abe79-111">Requirements</span></span>



| <span data-ttu-id="abe79-112">Требование</span><span class="sxs-lookup"><span data-stu-id="abe79-112">Requirement</span></span> | <span data-ttu-id="abe79-113">Значение</span><span class="sxs-lookup"><span data-stu-id="abe79-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe79-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="abe79-114">Redistributable</span></span><br/> | <span data-ttu-id="abe79-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="abe79-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="abe79-116">DLL</span><span class="sxs-lookup"><span data-stu-id="abe79-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="abe79-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abe79-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe79-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abe79-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe79-119">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="abe79-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
