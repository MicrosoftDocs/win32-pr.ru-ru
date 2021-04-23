---
description: Метод SetEncryptionKey задает ключ шифрования, необходимый для расшифровки сеанса, или указывает механизм для получения используемого ключа внешним средством.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Метод Итконнектион:: SetEncryptionKey (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685313"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="140e8-103">Метод Итконнектион:: SetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="140e8-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="140e8-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="140e8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="140e8-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="140e8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="140e8-106">Метод **SetEncryptionKey** задает ключ шифрования, необходимый для расшифровки сеанса, или указывает механизм для получения используемого ключа внешним средством.</span><span class="sxs-lookup"><span data-stu-id="140e8-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="140e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="140e8-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="140e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="140e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140e8-109">*пкэйтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="140e8-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140e8-110">Указатель на **строку BSTR** , содержащую тип ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="140e8-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="140e8-111">*ппкэйдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="140e8-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140e8-112">Указатель на **строку BSTR** , содержащую сведения о ключе шифрования.</span><span class="sxs-lookup"><span data-stu-id="140e8-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140e8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="140e8-113">Return value</span></span>

<span data-ttu-id="140e8-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="140e8-114">This method can return one of these values.</span></span>



| <span data-ttu-id="140e8-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="140e8-115">Return code</span></span>                                                                          | <span data-ttu-id="140e8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="140e8-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="140e8-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="140e8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="140e8-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="140e8-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="140e8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="140e8-119">Remarks</span></span>

<span data-ttu-id="140e8-120">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметров *пкэйтипе* и *ппкэйдата* .</span><span class="sxs-lookup"><span data-stu-id="140e8-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="140e8-121">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменные больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="140e8-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="140e8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="140e8-122">Requirements</span></span>



| <span data-ttu-id="140e8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="140e8-123">Requirement</span></span> | <span data-ttu-id="140e8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="140e8-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="140e8-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="140e8-125">TAPI version</span></span><br/> | <span data-ttu-id="140e8-126">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="140e8-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="140e8-127">Header</span><span class="sxs-lookup"><span data-stu-id="140e8-127">Header</span></span><br/>       | <dl> <span data-ttu-id="140e8-128"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="140e8-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="140e8-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="140e8-129">Library</span></span><br/>      | <dl> <span data-ttu-id="140e8-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="140e8-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="140e8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="140e8-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="140e8-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140e8-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="140e8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="140e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140e8-134">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="140e8-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

