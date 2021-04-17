---
title: Иконфигасфвритер Жеткуррентпрофилеид, метод
description: Метод Жеткуррентпрофилеид извлекает идентификатор текущего профиля. (Только для профилей Windows Media формата 4,0.)
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Формат Windows Media, Жеткуррентпрофилеид метод
- Жеткуррентпрофилеид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофилеид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691564"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="b9a88-107">Метод Иконфигасфвритер:: Жеткуррентпрофилеид</span><span class="sxs-lookup"><span data-stu-id="b9a88-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="b9a88-108">Метод **жеткуррентпрофилеид** извлекает идентификатор текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="b9a88-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="b9a88-109">(Только для профилей Windows Media формата 4,0.)</span><span class="sxs-lookup"><span data-stu-id="b9a88-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a88-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9a88-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="b9a88-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9a88-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a88-112">*пдвпрофилеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b9a88-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a88-113">Указатель на переменную типа **DWORD** , которая получает идентификатор текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="b9a88-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a88-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9a88-114">Return value</span></span>

<span data-ttu-id="b9a88-115">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b9a88-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b9a88-116">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9a88-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a88-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9a88-117">Remarks</span></span>

<span data-ttu-id="b9a88-118">Этот метод устарел, так как в нем предполагается наличие профилей пакета SDK для формата Windows Media версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="b9a88-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="b9a88-119">Вместо этого используйте [**иконфигасфвритер:: жеткуррентпрофиле**](iconfigasfwriter-getcurrentprofile.md) или [**Иконфигасфвритер:: жеткуррентпрофилегуид**](iconfigasfwriter-getcurrentprofileguid.md) , чтобы правильно указать профиль для версии 7,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="b9a88-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9a88-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9a88-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9a88-121">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9a88-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 