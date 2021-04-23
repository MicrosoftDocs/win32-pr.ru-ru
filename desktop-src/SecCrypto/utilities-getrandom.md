---
description: Создает безопасное случайное число с помощью поставщика служб шифрования (CSP) по умолчанию.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Метод Utilities. Random
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688793"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="b01d0-103">Метод Utilities. Random</span><span class="sxs-lookup"><span data-stu-id="b01d0-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="b01d0-104">\[Метод **Random** доступен для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="b01d0-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="b01d0-105">Метод **Random** создает безопасное случайное число с помощью [*поставщика служб шифрования*](../secgloss/c-gly.md) по умолчанию (CSP).</span><span class="sxs-lookup"><span data-stu-id="b01d0-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b01d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b01d0-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b01d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b01d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b01d0-108">*Длина* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b01d0-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b01d0-109">Длина создаваемого случайного числа в байтах.</span><span class="sxs-lookup"><span data-stu-id="b01d0-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="b01d0-110">Значение по умолчанию — 8 байт.</span><span class="sxs-lookup"><span data-stu-id="b01d0-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b01d0-111">*Енкодингтипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b01d0-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b01d0-112">Значение перечисления [**\_ \_ типа CAPICOM Encoding**](capicom-encoding-type.md) , указывающее тип кодировки, используемой для сгенерированного случайного числа.</span><span class="sxs-lookup"><span data-stu-id="b01d0-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="b01d0-113">Значение по умолчанию — \_ двоичная кодировка CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="b01d0-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="b01d0-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b01d0-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b01d0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b01d0-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="b01d0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b01d0-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="b01d0-117"><dt>**CAPICOM \_ кодирует \_ ANY**</dt></span><span class="sxs-lookup"><span data-stu-id="b01d0-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="b01d0-118">Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования.</span><span class="sxs-lookup"><span data-stu-id="b01d0-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="b01d0-119">Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64.</span><span class="sxs-lookup"><span data-stu-id="b01d0-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="b01d0-120">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b01d0-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="b01d0-121"><dt>**CAPICOM \_ кодирует \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="b01d0-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="b01d0-122">Данные сохраняются в виде строки в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="b01d0-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="b01d0-123"><dt>**\_двоичная кодировка CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b01d0-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="b01d0-124">Данные сохраняются в виде чисто двоичной последовательности.</span><span class="sxs-lookup"><span data-stu-id="b01d0-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b01d0-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b01d0-125">Return value</span></span>

<span data-ttu-id="b01d0-126">Генерируемое случайным образом число байтов *длиной* в байтах с указанной кодировкой.</span><span class="sxs-lookup"><span data-stu-id="b01d0-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01d0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b01d0-127">Requirements</span></span>



| <span data-ttu-id="b01d0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b01d0-128">Requirement</span></span> | <span data-ttu-id="b01d0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b01d0-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01d0-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b01d0-130">Redistributable</span></span><br/> | <span data-ttu-id="b01d0-131">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b01d0-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b01d0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b01d0-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="b01d0-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01d0-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b01d0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b01d0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01d0-135">**Служебные программы**</span><span class="sxs-lookup"><span data-stu-id="b01d0-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
