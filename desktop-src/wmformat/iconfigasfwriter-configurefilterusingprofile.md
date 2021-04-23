---
title: Иконфигасфвритер Конфигурефилтерусингпрофиле, метод
description: Метод Конфигурефилтерусингпрофиле является рекомендуемым способом задания профиля. Он настраивает фильтр для записи ASF-файла на основе заданного профиля, определенного приложением.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Формат Windows Media, Конфигурефилтерусингпрофиле метод
- Конфигурефилтерусингпрофиле метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Конфигурефилтерусингпрофиле
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700923"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="93727-107">Метод Иконфигасфвритер:: Конфигурефилтерусингпрофиле</span><span class="sxs-lookup"><span data-stu-id="93727-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="93727-108">Метод **конфигурефилтерусингпрофиле** является рекомендуемым способом задания профиля.</span><span class="sxs-lookup"><span data-stu-id="93727-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="93727-109">Он настраивает фильтр для записи ASF-файла на основе заданного профиля, определенного приложением.</span><span class="sxs-lookup"><span data-stu-id="93727-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="93727-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93727-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="93727-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="93727-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93727-112">*ппрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93727-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93727-113">Указатель на интерфейс [**ивмпрофиле**](iwmprofile.md) в определяемом приложением профиле.</span><span class="sxs-lookup"><span data-stu-id="93727-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93727-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93727-114">Return value</span></span>

<span data-ttu-id="93727-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="93727-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="93727-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="93727-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="93727-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="93727-117">Return code</span></span>                                                                                         | <span data-ttu-id="93727-118">Описание</span><span class="sxs-lookup"><span data-stu-id="93727-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="93727-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="93727-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="93727-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="93727-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="93727-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="93727-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="93727-122">Недопустимый указатель интерфейса **ивмпрофиле** .</span><span class="sxs-lookup"><span data-stu-id="93727-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="93727-123"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="93727-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="93727-124">Граф остановлен.</span><span class="sxs-lookup"><span data-stu-id="93727-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="93727-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93727-125">Remarks</span></span>

<span data-ttu-id="93727-126">В случае успеха этот метод приведет к отправке приложению события **\_ \_ изменения в диаграмме EC** .</span><span class="sxs-lookup"><span data-stu-id="93727-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="93727-127">Этот метод используется для настройки модуля записи с помощью настраиваемого профиля серии Windows Media 9, созданного (или загруженного из существующего пркс-файла) с использованием методов пакета SDK формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="93727-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="93727-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93727-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="93727-129">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93727-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

