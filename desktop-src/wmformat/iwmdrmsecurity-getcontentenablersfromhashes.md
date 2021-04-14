---
title: Метод Ивмдрмсекурити Жетконтентенаблерсфромхашес (Вмдрмсдк. h)
description: Метод Жетконтентенаблерсфромхашес получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе хэшированных сертификатов.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Формат Windows Media, Жетконтентенаблерсфромхашес метод
- Жетконтентенаблерсфромхашес метод Windows Media Format, интерфейс Ивмдрмсекурити
- Интерфейс Ивмдрмсекурити Windows Media Format, метод Жетконтентенаблерсфромхашес
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648011"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="b7cc3-106">Метод Ивмдрмсекурити:: Жетконтентенаблерсфромхашес</span><span class="sxs-lookup"><span data-stu-id="b7cc3-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="b7cc3-107">Метод **жетконтентенаблерсфромхашес** получает интерфейсы включения содержимого, которые обеспечивают возобновление компонентов на основе хэшированных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7cc3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7cc3-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="b7cc3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7cc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7cc3-110">*ргпбцерсашес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7cc3-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cc3-111">Массив хэшей сертификатов для получения содержимого созидателями.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="b7cc3-112">*кцертс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7cc3-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cc3-113">Число сертификатов для получения содержимого созидателями.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="b7cc3-114">Число элементов в массиве *ргпбцерсашес* .</span><span class="sxs-lookup"><span data-stu-id="b7cc3-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="b7cc3-115">*хресулсинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7cc3-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cc3-116">Возвращенное значение, полученное из операции, которая завершилась сбоем из-за отозванного сертификата.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="b7cc3-117">Если вы не вызываете в ответ на вызов метода со сбоем, задайте для параметра значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="b7cc3-118">*пргконтентенаблерс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b7cc3-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cc3-119">Массив, который получает адреса только что созданных интерфейсов **имфконтентенаблер** .</span><span class="sxs-lookup"><span data-stu-id="b7cc3-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="b7cc3-120">Задайте значение **null** , чтобы получить количество созидателями содержимого в параметре *пкконтентенаблерс* .</span><span class="sxs-lookup"><span data-stu-id="b7cc3-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b7cc3-121">*пкконтентенаблерс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b7cc3-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7cc3-122">Число элементов в массиве *пргконтентенаблерс* .</span><span class="sxs-lookup"><span data-stu-id="b7cc3-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="b7cc3-123">Если *пргконтентенаблерс* имеет **значение NULL**, это значение устанавливается равным числу необходимых созидателями содержимого на выходе.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7cc3-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7cc3-124">Return value</span></span>

<span data-ttu-id="b7cc3-125">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7cc3-126">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7cc3-127">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b7cc3-127">Return code</span></span>                                                                          | <span data-ttu-id="b7cc3-128">Описание</span><span class="sxs-lookup"><span data-stu-id="b7cc3-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b7cc3-129"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b7cc3-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b7cc3-130">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7cc3-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7cc3-131">Remarks</span></span>

<span data-ttu-id="b7cc3-132">Если вы используете интерфейс **имфконтентенаблер** для обновления отозванных компонентов, необходимо уточнить процесс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="b7cc3-133">Это уточнение необходимо, так как процесс обновления отправляет данные с клиентского компьютера на веб-сайт корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="b7cc3-134">При вызове **имфконтентенаблер:: аутоматиценабле** программа включения содержимого запускает браузер по умолчанию с адресом службы обновления на веб-сайте Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="b7cc3-135">Уникальный идентификатор, идентифицирующий отозванный компонент, передается в службу обновления.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="b7cc3-136">Затем служба перенаправляет браузер на веб-страницу, с которой пользователь может загрузить и установить новую версию отозванного компонента.</span><span class="sxs-lookup"><span data-stu-id="b7cc3-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cc3-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b7cc3-137">Requirements</span></span>



| <span data-ttu-id="b7cc3-138">Требование</span><span class="sxs-lookup"><span data-stu-id="b7cc3-138">Requirement</span></span> | <span data-ttu-id="b7cc3-139">Значение</span><span class="sxs-lookup"><span data-stu-id="b7cc3-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cc3-140">Header</span><span class="sxs-lookup"><span data-stu-id="b7cc3-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b7cc3-141"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7cc3-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7cc3-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7cc3-142">Library</span></span><br/> | <dl> <span data-ttu-id="b7cc3-143"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7cc3-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7cc3-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7cc3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cc3-145">**Интерфейс Ивмдрмсекурити**</span><span class="sxs-lookup"><span data-stu-id="b7cc3-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





