---
description: Выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Метод Иеаксисервицекаллбакк:: Верифифиле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546530"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="c570b-103">Метод Иеаксисервицекаллбакк:: Верифифиле</span><span class="sxs-lookup"><span data-stu-id="c570b-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="c570b-104">Метод **верифифиле** выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="c570b-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="c570b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c570b-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c570b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c570b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c570b-107">*бстрфилеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c570b-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c570b-108">URL-адрес объекта ActiveX для проверки.</span><span class="sxs-lookup"><span data-stu-id="c570b-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="c570b-109">*бстраппроведфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c570b-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c570b-110">Имя файла, в который был скачан CAB-файл, связанный с объектом ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c570b-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c570b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c570b-111">Return value</span></span>

<span data-ttu-id="c570b-112">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c570b-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="c570b-113">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c570b-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c570b-114">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="c570b-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="c570b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c570b-115">Requirements</span></span>



| <span data-ttu-id="c570b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c570b-116">Requirement</span></span> | <span data-ttu-id="c570b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c570b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c570b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c570b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c570b-119">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="c570b-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c570b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c570b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c570b-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c570b-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="c570b-122">IID</span><span class="sxs-lookup"><span data-stu-id="c570b-122">IID</span></span><br/>                      | <span data-ttu-id="c570b-123">IID \_ иеаксисервицекаллбакк определен как 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="c570b-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="c570b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c570b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c570b-125">**иеаксисервицекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c570b-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

