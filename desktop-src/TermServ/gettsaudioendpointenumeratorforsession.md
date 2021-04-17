---
title: Функция обратного вызова Жеттсаудиоендпоинтенумераторфорсессион
description: Возвращает ссылку на перечислитель конечной точки аудио для указанного идентификатора сеанса.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции обратного вызова Жеттсаудиоендпоинтенумераторфорсессион
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682083"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="fe598-104">Функция обратного вызова Жеттсаудиоендпоинтенумераторфорсессион</span><span class="sxs-lookup"><span data-stu-id="fe598-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="fe598-105">Возвращает ссылку на перечислитель конечной точки аудио для указанного идентификатора сеанса.</span><span class="sxs-lookup"><span data-stu-id="fe598-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="fe598-106">Потребители этого перечислителя конечной точки аудио, такие как MMDevAPI.dll, вызывают эту функцию, чтобы получить перечислитель конечных точек аудио в службы удаленных рабочих столовном сеансе.</span><span class="sxs-lookup"><span data-stu-id="fe598-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe598-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe598-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="fe598-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe598-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe598-109">*Идентификатор сеанса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe598-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe598-110">Идентификатор сеанса службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fe598-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="fe598-111">*ппендпоинтенумератор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe598-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe598-112">Адрес указателя на интерфейс [**иммдевицеенумератор**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="fe598-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe598-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe598-113">Return value</span></span>

<span data-ttu-id="fe598-114">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fe598-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe598-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe598-115">Remarks</span></span>

<span data-ttu-id="fe598-116">Эта функция не определена в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="fe598-116">This function is not defined in a header file.</span></span> <span data-ttu-id="fe598-117">Эту функцию следует реализовать и экспортировать в пользовательский перечислитель конечной точки и использовать сигнатуру, приведенную в блоке синтаксиса ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="fe598-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe598-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fe598-118">Requirements</span></span>



| <span data-ttu-id="fe598-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fe598-119">Requirement</span></span> | <span data-ttu-id="fe598-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fe598-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="fe598-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe598-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe598-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe598-122">None supported</span></span><br/>         |
| <span data-ttu-id="fe598-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe598-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe598-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe598-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe598-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe598-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe598-126">Реализация пользовательского перечислителя конечной точки аудио</span><span class="sxs-lookup"><span data-stu-id="fe598-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="fe598-127">**иммдевицеенумератор**</span><span class="sxs-lookup"><span data-stu-id="fe598-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

