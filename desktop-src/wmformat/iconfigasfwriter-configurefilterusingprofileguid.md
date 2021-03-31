---
title: Иконфигасфвритер Конфигурефилтерусингпрофилегуид, метод
description: Метод Конфигурефилтерусингпрофилегуид настраивает фильтр для записи файла ASF на основе указанного заранее заданного профиля. (Не рекомендуется.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Формат Windows Media, Конфигурефилтерусингпрофилегуид метод
- Конфигурефилтерусингпрофилегуид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Конфигурефилтерусингпрофилегуид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533410"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="febfa-107">Метод Иконфигасфвритер:: Конфигурефилтерусингпрофилегуид</span><span class="sxs-lookup"><span data-stu-id="febfa-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="febfa-108">Метод **конфигурефилтерусингпрофилегуид** настраивает фильтр для записи файла ASF на основе указанного заранее заданного профиля.</span><span class="sxs-lookup"><span data-stu-id="febfa-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="febfa-109">(Не рекомендуется.)</span><span class="sxs-lookup"><span data-stu-id="febfa-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="febfa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="febfa-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="febfa-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="febfa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febfa-112">*гуидпрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="febfa-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="febfa-113">**Идентификатор GUID** , определяющий профиль, как определено в файле заголовка пакета SDK для формата Windows Media вмсиспрф. h.</span><span class="sxs-lookup"><span data-stu-id="febfa-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febfa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="febfa-114">Return value</span></span>

<span data-ttu-id="febfa-115">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="febfa-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="febfa-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="febfa-116">Return code</span></span>                                                                                         | <span data-ttu-id="febfa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="febfa-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="febfa-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="febfa-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="febfa-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="febfa-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="febfa-120"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="febfa-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="febfa-121">Недопустимый профиль.</span><span class="sxs-lookup"><span data-stu-id="febfa-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="febfa-122"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="febfa-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="febfa-123">Граф фильтра остановлен.</span><span class="sxs-lookup"><span data-stu-id="febfa-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="febfa-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="febfa-124">Remarks</span></span>

<span data-ttu-id="febfa-125">Начиная с Windows Media Format SDK серии 9 не были определены новые профили системы.</span><span class="sxs-lookup"><span data-stu-id="febfa-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="febfa-126">С этим методом можно использовать только идентификаторы GUID системного профиля версии 8 (или более ранней).</span><span class="sxs-lookup"><span data-stu-id="febfa-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="febfa-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="febfa-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="febfa-128">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="febfa-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

