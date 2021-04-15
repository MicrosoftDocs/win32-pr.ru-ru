---
description: Возвращает строковое представление закодированных данных.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Енкодеддата. Format, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648967"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="24a21-103">Енкодеддата. Format, метод</span><span class="sxs-lookup"><span data-stu-id="24a21-103">EncodedData.Format method</span></span>

<span data-ttu-id="24a21-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24a21-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="24a21-105">Вместо этого используйте [**класс асненкодеддата**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="24a21-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="24a21-106">Метод **Format** возвращает строковое представление закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="24a21-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a21-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24a21-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="24a21-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="24a21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a21-109">*бмултилинес* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="24a21-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24a21-110">Логическое значение, указывающее, содержит ли возвращаемая строка несколько строк.</span><span class="sxs-lookup"><span data-stu-id="24a21-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="24a21-111">Если **значение — true**, возвращаемая строка может содержать несколько строк, разделенных **вбкрлф**.</span><span class="sxs-lookup"><span data-stu-id="24a21-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="24a21-112">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="24a21-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24a21-113">Return value</span></span>

<span data-ttu-id="24a21-114">Понятная для человека строка, представляющая закодированные данные.</span><span class="sxs-lookup"><span data-stu-id="24a21-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="24a21-115">Если элемент CAPICOM не понимает закодированные данные, возвращается шестнадцатеричное представление данных.</span><span class="sxs-lookup"><span data-stu-id="24a21-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a21-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24a21-116">Remarks</span></span>

<span data-ttu-id="24a21-117">Формат возвращаемой строки может изменяться в разных версиях элемента CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="24a21-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="24a21-118">Не полагайтесь на определенный формат в приложении.</span><span class="sxs-lookup"><span data-stu-id="24a21-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a21-119">Требования</span><span class="sxs-lookup"><span data-stu-id="24a21-119">Requirements</span></span>



| <span data-ttu-id="24a21-120">Требование</span><span class="sxs-lookup"><span data-stu-id="24a21-120">Requirement</span></span> | <span data-ttu-id="24a21-121">Значение</span><span class="sxs-lookup"><span data-stu-id="24a21-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a21-122">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="24a21-122">End of client support</span></span><br/> | <span data-ttu-id="24a21-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24a21-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="24a21-124">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="24a21-124">End of server support</span></span><br/> | <span data-ttu-id="24a21-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24a21-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="24a21-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="24a21-126">Redistributable</span></span><br/>       | <span data-ttu-id="24a21-127">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="24a21-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="24a21-128">DLL</span><span class="sxs-lookup"><span data-stu-id="24a21-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="24a21-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a21-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a21-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24a21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a21-131">**енкодеддата**</span><span class="sxs-lookup"><span data-stu-id="24a21-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
