---
title: Иконфигасфвритер Жеткуррентпрофилегуид, метод
description: Метод Жеткуррентпрофилегуид извлекает текущий GUID профиля системы Windows Media.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Формат Windows Media, Жеткуррентпрофилегуид метод
- Жеткуррентпрофилегуид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофилегуид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338796"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="294b0-106">Метод Иконфигасфвритер:: Жеткуррентпрофилегуид</span><span class="sxs-lookup"><span data-stu-id="294b0-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="294b0-107">Метод **жеткуррентпрофилегуид** ИЗВЛЕКАЕТ текущий GUID профиля системы Windows Media.</span><span class="sxs-lookup"><span data-stu-id="294b0-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="294b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="294b0-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="294b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="294b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="294b0-110">*ппрофилегуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="294b0-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="294b0-111">Указатель на переменную типа **GUID** , определяющую текущий системный профиль, используемый фильтром.</span><span class="sxs-lookup"><span data-stu-id="294b0-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="294b0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="294b0-112">Return value</span></span>

<span data-ttu-id="294b0-113">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="294b0-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="294b0-114">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="294b0-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="294b0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="294b0-115">Remarks</span></span>

<span data-ttu-id="294b0-116">Этот метод не используется с пользовательскими профилями (включая все профили, включающие потоки, использующие аудиокодеки Windows Media и видеокодеки), так как все такие профили создаются приложениями и не имеют идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="294b0-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="294b0-117">Если системный профиль не загружен, *ппрофилегуид* будет иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="294b0-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="294b0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="294b0-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="294b0-119">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="294b0-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 