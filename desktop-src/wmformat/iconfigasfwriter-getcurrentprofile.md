---
title: Иконфигасфвритер Жеткуррентпрофиле, метод
description: Метод Жеткуррентпрофиле извлекает профиль, определяемый приложением.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Формат Windows Media, Жеткуррентпрофиле метод
- Жеткуррентпрофиле метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Жеткуррентпрофиле
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710303"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="3f698-106">Метод Иконфигасфвритер:: Жеткуррентпрофиле</span><span class="sxs-lookup"><span data-stu-id="3f698-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="3f698-107">Метод **жеткуррентпрофиле** извлекает профиль, определяемый приложением.</span><span class="sxs-lookup"><span data-stu-id="3f698-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f698-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f698-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="3f698-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f698-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f698-110">*пппрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3f698-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f698-111">Адрес указателя, получающего интерфейс [**ивмпрофиле**](iwmprofile.md) определяемого приложением профиля.</span><span class="sxs-lookup"><span data-stu-id="3f698-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f698-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f698-112">Return value</span></span>

<span data-ttu-id="3f698-113">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3f698-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3f698-114">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f698-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f698-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f698-115">Remarks</span></span>

<span data-ttu-id="3f698-116">Если метод завершается успешно, возвращаемый им указатель **ивмпрофиле** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="3f698-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="3f698-117">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="3f698-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f698-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f698-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f698-119">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f698-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 