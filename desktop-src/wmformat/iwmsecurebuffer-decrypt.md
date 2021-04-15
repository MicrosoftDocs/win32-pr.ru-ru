---
title: Метод дешифровки Ивмсекуребуффер (Вмдрмсдк. h)
description: Метод дешифровки расшифровывает указатель данных, который был зашифрован путем вызова метода Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Расшифровка метода Windows Media Format
- Метод расшифровки формата Windows Media Format, интерфейс Ивмсекуребуффер
- Интерфейс Ивмсекуребуффер интерфейса Windows Media Format, метод дешифрации
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669478"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="8ffdc-106">Ивмсекуребуффер: метод:D екрипт</span><span class="sxs-lookup"><span data-stu-id="8ffdc-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="8ffdc-107">Метод **дешифровки** расшифровывает указатель данных, который был зашифрован путем вызова метода [**Encrypt**](iwmsecurebuffer-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffdc-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffdc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ffdc-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="8ffdc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ffdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffdc-110">*псекуречаннел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ffdc-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffdc-111">Указатель на интерфейс безопасного канала, содержащий указатель зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="8ffdc-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffdc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ffdc-112">Return value</span></span>

<span data-ttu-id="8ffdc-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8ffdc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ffdc-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ffdc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ffdc-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8ffdc-115">Return code</span></span>                                                                          | <span data-ttu-id="8ffdc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8ffdc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8ffdc-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8ffdc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8ffdc-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="8ffdc-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ffdc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ffdc-119">Remarks</span></span>

<span data-ttu-id="8ffdc-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="8ffdc-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffdc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8ffdc-121">Requirements</span></span>



| <span data-ttu-id="8ffdc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8ffdc-122">Requirement</span></span> | <span data-ttu-id="8ffdc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8ffdc-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffdc-124">Header</span><span class="sxs-lookup"><span data-stu-id="8ffdc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8ffdc-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ffdc-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ffdc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ffdc-126">Library</span></span><br/> | <dl> <span data-ttu-id="8ffdc-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ffdc-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffdc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ffdc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffdc-129">**Шифрование**</span><span class="sxs-lookup"><span data-stu-id="8ffdc-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="8ffdc-130">**Интерфейс Ивмсекуребуффер**</span><span class="sxs-lookup"><span data-stu-id="8ffdc-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





