---
description: Удаляет объект сертификата из коллекции получателей.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Метод Recipients. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685304"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="1b31a-103">Метод Recipients. Remove</span><span class="sxs-lookup"><span data-stu-id="1b31a-103">Recipients.Remove method</span></span>

<span data-ttu-id="1b31a-104">\[Метод **Remove** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1b31a-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1b31a-105">Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1b31a-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1b31a-106">Метод **Remove** удаляет объект [**сертификата**](certificate.md) из коллекции [**получателей**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="1b31a-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b31a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b31a-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="1b31a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b31a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b31a-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b31a-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b31a-110">Индекс объекта [**сертификата**](certificate.md) , который необходимо удалить из коллекции.</span><span class="sxs-lookup"><span data-stu-id="1b31a-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b31a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b31a-111">Return value</span></span>

<span data-ttu-id="1b31a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1b31a-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b31a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1b31a-113">Requirements</span></span>



| <span data-ttu-id="1b31a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1b31a-114">Requirement</span></span> | <span data-ttu-id="1b31a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1b31a-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b31a-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1b31a-116">Redistributable</span></span><br/> | <span data-ttu-id="1b31a-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b31a-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1b31a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1b31a-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="1b31a-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b31a-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b31a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b31a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b31a-121">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="1b31a-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="1b31a-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="1b31a-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
