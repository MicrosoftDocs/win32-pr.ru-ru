---
description: Метод GetEncryptionKey получает ключ шифрования.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Метод Итконнектион:: GetEncryptionKey (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685319"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="86d68-103">Метод Итконнектион:: GetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="86d68-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="86d68-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="86d68-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86d68-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="86d68-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86d68-106">Метод **GetEncryptionKey** получает ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="86d68-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d68-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86d68-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="86d68-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="86d68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d68-109">*ппкэйтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86d68-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d68-110">Указатель на **строку BSTR** , содержащую тип ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="86d68-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="86d68-111">*пфвалидкэйдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86d68-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d68-112">Указывает на допустимость данных ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="86d68-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="86d68-113">*ппкэйдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="86d68-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86d68-114">Указатель на **строку BSTR** , содержащую данные ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="86d68-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d68-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86d68-115">Return value</span></span>

<span data-ttu-id="86d68-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="86d68-116">This method can return one of these values.</span></span>



| <span data-ttu-id="86d68-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="86d68-117">Return code</span></span>                                                                                   | <span data-ttu-id="86d68-118">Описание</span><span class="sxs-lookup"><span data-stu-id="86d68-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86d68-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86d68-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="86d68-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="86d68-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86d68-122">Параметр *ппкэйтипе, пфвалидкэйдата* или *ппкэйдата* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="86d68-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="86d68-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86d68-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="86d68-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="86d68-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="86d68-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="86d68-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="86d68-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="86d68-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="86d68-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="86d68-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86d68-129">Remarks</span></span>

<span data-ttu-id="86d68-130">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметров *ппкэйтипе* и *ппкэйдата* .</span><span class="sxs-lookup"><span data-stu-id="86d68-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d68-131">Требования</span><span class="sxs-lookup"><span data-stu-id="86d68-131">Requirements</span></span>



| <span data-ttu-id="86d68-132">Требование</span><span class="sxs-lookup"><span data-stu-id="86d68-132">Requirement</span></span> | <span data-ttu-id="86d68-133">Значение</span><span class="sxs-lookup"><span data-stu-id="86d68-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86d68-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="86d68-134">TAPI version</span></span><br/> | <span data-ttu-id="86d68-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="86d68-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86d68-136">Header</span><span class="sxs-lookup"><span data-stu-id="86d68-136">Header</span></span><br/>       | <dl> <span data-ttu-id="86d68-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="86d68-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86d68-138">Library</span></span><br/>      | <dl> <span data-ttu-id="86d68-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86d68-140">DLL</span><span class="sxs-lookup"><span data-stu-id="86d68-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="86d68-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86d68-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d68-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86d68-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d68-143">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="86d68-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

