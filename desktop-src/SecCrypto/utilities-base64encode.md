---
description: Кодирует строку в кодировке Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Метод Utilities. Base64Encode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685377"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="0ee05-103">Метод Utilities. Base64Encode</span><span class="sxs-lookup"><span data-stu-id="0ee05-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="0ee05-104">\[Метод **Base64Encode** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="0ee05-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="0ee05-105">Метод **Base64Encode** кодирует строку в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="0ee05-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee05-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee05-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="0ee05-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ee05-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee05-108">*Сркстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ee05-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee05-109">Строка для кодирования в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="0ee05-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee05-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ee05-110">Return value</span></span>

<span data-ttu-id="0ee05-111">Строка в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="0ee05-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee05-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ee05-112">Remarks</span></span>

<span data-ttu-id="0ee05-113">Кодировка base64 — это схема, используемая для передачи двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="0ee05-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="0ee05-114">Base64 обрабатывает данные в виде 24-разрядных групп, сопоставляя эти данные с четырьмя закодированными символами.</span><span class="sxs-lookup"><span data-stu-id="0ee05-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="0ee05-115">Кодировка base64 иногда называется кодировкой 3 – 4.</span><span class="sxs-lookup"><span data-stu-id="0ee05-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="0ee05-116">Каждый 6 бит 24-разрядной группы используется в качестве индекса в таблице сопоставления (в кодировке Base64) для получения символа для закодированных данных.</span><span class="sxs-lookup"><span data-stu-id="0ee05-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="0ee05-117">Закодированные данные имеют длину строк, которая ограничена 76 символами.</span><span class="sxs-lookup"><span data-stu-id="0ee05-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee05-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee05-118">Requirements</span></span>



| <span data-ttu-id="0ee05-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee05-119">Requirement</span></span> | <span data-ttu-id="0ee05-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee05-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee05-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0ee05-121">Redistributable</span></span><br/> | <span data-ttu-id="0ee05-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ee05-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0ee05-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee05-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="0ee05-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee05-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee05-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee05-126">**Служебные программы**</span><span class="sxs-lookup"><span data-stu-id="0ee05-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




