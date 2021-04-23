---
description: Устанавливает указанный объект ActiveX.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Метод Иеаксисистеминсталлер:: Инитиализесистеминсталлер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912431"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="c0999-103">Метод Иеаксисистеминсталлер:: Инитиализесистеминсталлер</span><span class="sxs-lookup"><span data-stu-id="c0999-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="c0999-104">Метод **инитиализесистеминсталлер** устанавливает указанный объект ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c0999-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0999-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0999-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="c0999-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0999-107">*бструрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0999-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0999-108">URL-адрес устанавливаемого объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c0999-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="c0999-109">*двклиентпид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0999-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0999-110">Идентификатор процесса вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="c0999-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="c0999-111">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0999-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0999-112">Указатель на экземпляр интерфейса [**иеаксисервицекаллбакк**](ieaxiservicecallback.md) , который проверяет, разрешена ли установка объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c0999-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="c0999-113">*пбстрнонце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c0999-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0999-114">Контекст, который можно использовать для совместного использования сведений о состоянии в вызовах других методов, используемых для проверки и загрузки объекта ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c0999-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0999-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0999-115">Return value</span></span>

<span data-ttu-id="c0999-116">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c0999-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="c0999-117">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c0999-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c0999-118">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="c0999-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0999-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c0999-119">Requirements</span></span>



| <span data-ttu-id="c0999-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c0999-120">Requirement</span></span> | <span data-ttu-id="c0999-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c0999-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0999-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0999-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c0999-123">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="c0999-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0999-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0999-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c0999-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0999-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="c0999-126">IID</span><span class="sxs-lookup"><span data-stu-id="c0999-126">IID</span></span><br/>                      | <span data-ttu-id="c0999-127">IID \_ иеаксисистеминсталлер определен как a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="c0999-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="c0999-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0999-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0999-129">**иеаксисистеминсталлер**</span><span class="sxs-lookup"><span data-stu-id="c0999-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

