---
title: Метод Ивмсекуребуффер Encrypt (Вмдрмсдк. h)
description: Метод Encrypt шифрует указатель данных.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Шифрование метода Windows Media Format
- Шифрование метода Windows Media Format, интерфейс Ивмсекуребуффер
- Интерфейс Ивмсекуребуффер интерфейса Windows Media Format, метод Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708601"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="c2fd3-106">Метод Ивмсекуребуффер:: Encrypt</span><span class="sxs-lookup"><span data-stu-id="c2fd3-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="c2fd3-107">Метод **Encrypt** шифрует указатель данных.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2fd3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2fd3-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="c2fd3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2fd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2fd3-110">*псекуречаннел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2fd3-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2fd3-111">Указатель на интерфейс безопасного канала, содержащий указатель данных для шифрования.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2fd3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2fd3-112">Return value</span></span>

<span data-ttu-id="c2fd3-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2fd3-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2fd3-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c2fd3-115">Return code</span></span>                                                                          | <span data-ttu-id="c2fd3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c2fd3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c2fd3-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c2fd3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2fd3-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2fd3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2fd3-119">Remarks</span></span>

<span data-ttu-id="c2fd3-120">Используйте этот метод для шифрования указателей на данные, чтобы их можно было отправлять через границы DLL.</span><span class="sxs-lookup"><span data-stu-id="c2fd3-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2fd3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c2fd3-121">Requirements</span></span>



| <span data-ttu-id="c2fd3-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c2fd3-122">Requirement</span></span> | <span data-ttu-id="c2fd3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c2fd3-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fd3-124">Header</span><span class="sxs-lookup"><span data-stu-id="c2fd3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c2fd3-125"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2fd3-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2fd3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2fd3-126">Library</span></span><br/> | <dl> <span data-ttu-id="c2fd3-127"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2fd3-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2fd3-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2fd3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fd3-129">**расшифровка;**</span><span class="sxs-lookup"><span data-stu-id="c2fd3-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="c2fd3-130">**Интерфейс Ивмсекуребуффер**</span><span class="sxs-lookup"><span data-stu-id="c2fd3-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





