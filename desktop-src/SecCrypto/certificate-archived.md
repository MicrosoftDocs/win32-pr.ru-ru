---
description: Задает или получает логическое значение, указывающее, архивируется ли сертификат.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Заархивированное Свойство Certificate.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649111"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="a955f-103">Заархивированное Свойство Certificate.</span><span class="sxs-lookup"><span data-stu-id="a955f-103">Certificate.Archived property</span></span>

<span data-ttu-id="a955f-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a955f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a955f-105">Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a955f-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a955f-106">**Заархивированное** свойство задает или получает логическое значение, указывающее, архивируется ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="a955f-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="a955f-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a955f-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a955f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a955f-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a955f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a955f-109">Property value</span></span>

<span data-ttu-id="a955f-110">Логическое значение, указывающее, архивируется ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="a955f-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="a955f-111">Если **значение — true**, сертификат архивируется.</span><span class="sxs-lookup"><span data-stu-id="a955f-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="a955f-112">Обратите внимание, что изменение значения с **false** на **true** архивирует сертификат.</span><span class="sxs-lookup"><span data-stu-id="a955f-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="a955f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a955f-113">Remarks</span></span>

<span data-ttu-id="a955f-114">Это свойство вызывает CAPICOM \_ E \_ не \_ разрешено при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a955f-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="a955f-115">Архивный сертификат не отображается в пользовательском интерфейсе управления сертификатами.</span><span class="sxs-lookup"><span data-stu-id="a955f-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="a955f-116">Кроме того, архивные сертификаты не будут включены в метод [**Store. Open**](store-open.md) , если не \_ задано поле Открыть хранилище CAPICOM с \_ \_ \_ параметром archiveed.</span><span class="sxs-lookup"><span data-stu-id="a955f-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a955f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a955f-117">Requirements</span></span>



| <span data-ttu-id="a955f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a955f-118">Requirement</span></span> | <span data-ttu-id="a955f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a955f-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a955f-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a955f-120">End of client support</span></span><br/> | <span data-ttu-id="a955f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a955f-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a955f-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a955f-122">End of server support</span></span><br/> | <span data-ttu-id="a955f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a955f-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a955f-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a955f-124">Redistributable</span></span><br/>       | <span data-ttu-id="a955f-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a955f-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a955f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a955f-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a955f-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a955f-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
