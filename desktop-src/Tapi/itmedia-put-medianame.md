---
description: Метод размещения \_ MediaName задает имя носителя. К определенным носителям относятся аудио, видео, доска, текст и данные.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: 'Итмедиа: метод ut_MediaName:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675247"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="f1517-104">Итмедиа::p UT \_ MediaName метод</span><span class="sxs-lookup"><span data-stu-id="f1517-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="f1517-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f1517-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1517-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f1517-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1517-107">Метод **размещения \_ MediaName** задает имя носителя.</span><span class="sxs-lookup"><span data-stu-id="f1517-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="f1517-108">К определенным носителям относятся аудио, видео, доска, текст и данные.</span><span class="sxs-lookup"><span data-stu-id="f1517-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1517-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1517-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="f1517-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1517-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1517-111">*пмедианаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1517-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1517-112">Указатель на **строку BSTR** , содержащую имя носителя для задания.</span><span class="sxs-lookup"><span data-stu-id="f1517-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1517-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1517-113">Return value</span></span>

<span data-ttu-id="f1517-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f1517-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f1517-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f1517-115">Return code</span></span>                                                                                   | <span data-ttu-id="f1517-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f1517-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f1517-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1517-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f1517-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f1517-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f1517-120">Параметр *пмедианаме* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="f1517-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="f1517-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1517-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f1517-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f1517-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f1517-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1517-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f1517-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f1517-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="f1517-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f1517-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1517-127">Remarks</span></span>

<span data-ttu-id="f1517-128">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пмедианаме* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="f1517-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="f1517-129">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="f1517-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="f1517-130">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="f1517-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1517-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f1517-131">Requirements</span></span>



| <span data-ttu-id="f1517-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f1517-132">Requirement</span></span> | <span data-ttu-id="f1517-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f1517-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1517-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f1517-134">TAPI version</span></span><br/> | <span data-ttu-id="f1517-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f1517-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f1517-136">Header</span><span class="sxs-lookup"><span data-stu-id="f1517-136">Header</span></span><br/>       | <dl> <span data-ttu-id="f1517-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1517-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f1517-138">Library</span></span><br/>      | <dl> <span data-ttu-id="f1517-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f1517-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f1517-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1517-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1517-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1517-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1517-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1517-143">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="f1517-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="f1517-144">**Итмедиа:: Get \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="f1517-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

