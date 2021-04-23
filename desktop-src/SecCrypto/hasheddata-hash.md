---
description: Создает хэш указанной строки.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: Хашеддата. hash, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665315"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="d369e-103">Хашеддата. hash, метод</span><span class="sxs-lookup"><span data-stu-id="d369e-103">HashedData.Hash method</span></span>

<span data-ttu-id="d369e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d369e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d369e-105">Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d369e-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d369e-106">Метод **hash** создает хэш указанной строки.</span><span class="sxs-lookup"><span data-stu-id="d369e-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d369e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d369e-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="d369e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d369e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d369e-109">*неввал*</span><span class="sxs-lookup"><span data-stu-id="d369e-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="d369e-110">Строка, содержащая значение для хэширования.</span><span class="sxs-lookup"><span data-stu-id="d369e-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d369e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d369e-111">Return value</span></span>

<span data-ttu-id="d369e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d369e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d369e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d369e-113">Remarks</span></span>

<span data-ttu-id="d369e-114">Чтобы создать хэш большого объема данных, вызовите метод **хэширования** для каждого фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="d369e-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="d369e-115">Хэш каждого фрагмента данных объединяется со свойством [**value**](hasheddata-value.md) до тех пор, пока свойство не будет считано.</span><span class="sxs-lookup"><span data-stu-id="d369e-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="d369e-116">Содержимое свойства **value** сбрасывается при считывании свойства.</span><span class="sxs-lookup"><span data-stu-id="d369e-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="d369e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d369e-117">Requirements</span></span>



| <span data-ttu-id="d369e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d369e-118">Requirement</span></span> | <span data-ttu-id="d369e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d369e-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d369e-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d369e-120">End of client support</span></span><br/> | <span data-ttu-id="d369e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d369e-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d369e-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d369e-122">End of server support</span></span><br/> | <span data-ttu-id="d369e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d369e-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d369e-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d369e-124">Redistributable</span></span><br/>       | <span data-ttu-id="d369e-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d369e-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d369e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d369e-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d369e-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d369e-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
