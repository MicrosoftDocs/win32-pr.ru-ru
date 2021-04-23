---
description: Проверяет и скачивает объект ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Метод Иеаксисервице:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272454"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="39a6c-103">Метод Иеаксисервице:: Initialize</span><span class="sxs-lookup"><span data-stu-id="39a6c-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="39a6c-104">Метод **Initialize** проверяет и скачивает объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="39a6c-105">Если объект соответствует требованиям политики, этот метод инициализирует системный объект, который устанавливает объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a6c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39a6c-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="39a6c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a6c-108">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-109">Маркер родительского окна окна, которое пытается установить элемент управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-110">*двклиентпид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-111">Идентификатор процесса вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="39a6c-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-112">*бстрдесктоп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-113">Рабочий стол для объекта.</span><span class="sxs-lookup"><span data-stu-id="39a6c-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-114">*бстрклсид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-115">Идентификатор класса устанавливаемого объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-116">*бструрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-117">URL-адрес устанавливаемого объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-118">*пбстрнонце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-119">Контекст, который можно использовать для совместного использования сведений о состоянии в вызовах других методов, используемых для проверки и загрузки объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="39a6c-120">*пписинкброкеринтерфаце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39a6c-121">Указатель на экземпляр интерфейса [**иеаксисистеминсталлер**](ieaxisysteminstaller.md) , который устанавливает элемент управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a6c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39a6c-122">Return value</span></span>

<span data-ttu-id="39a6c-123">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="39a6c-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="39a6c-124">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="39a6c-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="39a6c-125">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="39a6c-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="39a6c-126">Описание</span><span class="sxs-lookup"><span data-stu-id="39a6c-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="39a6c-127"><dt>**Отношение доверия \_ E \_ \_ не является \_ доверенным**</dt> <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="39a6c-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="39a6c-128">Не следует устанавливать объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="39a6c-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39a6c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="39a6c-129">Requirements</span></span>



| <span data-ttu-id="39a6c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="39a6c-130">Requirement</span></span> | <span data-ttu-id="39a6c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="39a6c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a6c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39a6c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39a6c-133">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="39a6c-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39a6c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39a6c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39a6c-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="39a6c-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="39a6c-136">IID</span><span class="sxs-lookup"><span data-stu-id="39a6c-136">IID</span></span><br/>                      | <span data-ttu-id="39a6c-137">IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="39a6c-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="39a6c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a6c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a6c-139">**иеаксисервице**</span><span class="sxs-lookup"><span data-stu-id="39a6c-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




