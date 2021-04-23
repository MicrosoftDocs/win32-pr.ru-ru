---
title: Имедиарендерерактионинформатион Исволумеаваилабле, метод
description: Получает значение, указывающее, может ли ДМР настраивать уровень громкости звука.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API потоковой передачи мультимедиа метода Исволумеаваилабле
- API потоковой передачи мультимедиа метода Исволумеаваилабле, интерфейс Имедиарендерерактионинформатион
- API потоковой передачи мультимедиа интерфейса Имедиарендерерактионинформатион, метод Исволумеаваилабле
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133743"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="97160-106">Метод Имедиарендерерактионинформатион:: Исволумеаваилабле</span><span class="sxs-lookup"><span data-stu-id="97160-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="97160-107">Получает значение, указывающее, может ли ДМР настраивать уровень громкости звука.</span><span class="sxs-lookup"><span data-stu-id="97160-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="97160-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97160-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="97160-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="97160-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97160-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97160-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97160-111">Логическое значение, равное **true** , если ДМР поддерживает настройку уровня громкости звука и **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="97160-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97160-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97160-112">Return value</span></span>

<span data-ttu-id="97160-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="97160-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="97160-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="97160-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="97160-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="97160-115">Return code</span></span>                                                                          | <span data-ttu-id="97160-116">Описание</span><span class="sxs-lookup"><span data-stu-id="97160-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="97160-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="97160-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="97160-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="97160-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="97160-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97160-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97160-120">**имедиарендерерактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="97160-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

