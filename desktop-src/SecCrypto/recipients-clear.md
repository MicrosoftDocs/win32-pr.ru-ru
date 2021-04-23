---
description: Удаляет все объекты сертификата из коллекции получателей.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Метод Recipients. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685305"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="16467-103">Метод Recipients. Clear</span><span class="sxs-lookup"><span data-stu-id="16467-103">Recipients.Clear method</span></span>

<span data-ttu-id="16467-104">\[Метод **clear** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="16467-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="16467-105">Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="16467-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="16467-106">Метод **clear** удаляет все объекты [**сертификата**](certificate.md) из коллекции [**получателей**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="16467-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="16467-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16467-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="16467-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="16467-108">Parameters</span></span>

<span data-ttu-id="16467-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="16467-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="16467-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16467-110">Return value</span></span>

<span data-ttu-id="16467-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16467-111">This method does not return a value.</span></span> <span data-ttu-id="16467-112">Приложение, использующее этот метод, должно содержать код, обрабатывающий исключение, вызванное этим методом.</span><span class="sxs-lookup"><span data-stu-id="16467-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="16467-113">Требования</span><span class="sxs-lookup"><span data-stu-id="16467-113">Requirements</span></span>



| <span data-ttu-id="16467-114">Требование</span><span class="sxs-lookup"><span data-stu-id="16467-114">Requirement</span></span> | <span data-ttu-id="16467-115">Значение</span><span class="sxs-lookup"><span data-stu-id="16467-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16467-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="16467-116">Redistributable</span></span><br/> | <span data-ttu-id="16467-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="16467-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="16467-118">DLL</span><span class="sxs-lookup"><span data-stu-id="16467-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="16467-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16467-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16467-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16467-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16467-121">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="16467-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="16467-122">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="16467-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
