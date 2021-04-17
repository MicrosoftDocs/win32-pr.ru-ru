---
description: Извлекает хэшированные данные после успешного вызова метода хэширования.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: Хашеддата. Value, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665314"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="c15e3-103">Хашеддата. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="c15e3-103">HashedData.Value property</span></span>

<span data-ttu-id="c15e3-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c15e3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c15e3-105">Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="c15e3-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c15e3-106">Свойство **value** извлекает хэшированные данные после успешного вызова метода [**хэширования**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="c15e3-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="c15e3-107">Хэш-значение возвращается в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="c15e3-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="c15e3-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c15e3-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c15e3-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="c15e3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c15e3-110">Property value</span></span>

<span data-ttu-id="c15e3-111">Строка, содержащая хэшированные данные в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="c15e3-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="c15e3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c15e3-112">Remarks</span></span>

<span data-ttu-id="c15e3-113">Чтобы создать хэш большого объема данных, вызовите метод [**хэширования**](hasheddata-hash.md) для каждого фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="c15e3-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="c15e3-114">Хэш каждого фрагмента данных объединяется со свойством **value** до тех пор, пока свойство не будет считано.</span><span class="sxs-lookup"><span data-stu-id="c15e3-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="c15e3-115">Содержимое свойства **value** сбрасывается при считывании свойства.</span><span class="sxs-lookup"><span data-stu-id="c15e3-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15e3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c15e3-116">Requirements</span></span>



| <span data-ttu-id="c15e3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c15e3-117">Requirement</span></span> | <span data-ttu-id="c15e3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c15e3-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c15e3-119">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c15e3-119">End of client support</span></span><br/> | <span data-ttu-id="c15e3-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c15e3-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c15e3-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c15e3-121">End of server support</span></span><br/> | <span data-ttu-id="c15e3-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c15e3-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c15e3-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c15e3-123">Redistributable</span></span><br/>       | <span data-ttu-id="c15e3-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c15e3-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c15e3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c15e3-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c15e3-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c15e3-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15e3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c15e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15e3-128">**хашеддата**</span><span class="sxs-lookup"><span data-stu-id="c15e3-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
