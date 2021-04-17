---
title: Иконфигасфвритер Конфигурефилтерусингпрофилеид, метод
description: Метод Конфигурефилтерусингпрофилеид настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля. (Только для профилей Windows Media формата 4,0.)
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Формат Windows Media, Конфигурефилтерусингпрофилеид метод
- Конфигурефилтерусингпрофилеид метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Конфигурефилтерусингпрофилеид
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710304"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="25ca5-107">Метод Иконфигасфвритер:: Конфигурефилтерусингпрофилеид</span><span class="sxs-lookup"><span data-stu-id="25ca5-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="25ca5-108">Метод **конфигурефилтерусингпрофилеид** настраивает фильтр для записи ASF-файла с индексом идентификатора профиля из списка системного профиля.</span><span class="sxs-lookup"><span data-stu-id="25ca5-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="25ca5-109">(Только для профилей Windows Media формата 4,0.)</span><span class="sxs-lookup"><span data-stu-id="25ca5-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="25ca5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25ca5-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="25ca5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="25ca5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ca5-112">*двпрофилеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ca5-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ca5-113">Идентификатор профиля, определенный в версии 4,0 пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="25ca5-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ca5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25ca5-114">Return value</span></span>

<span data-ttu-id="25ca5-115">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25ca5-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="25ca5-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="25ca5-116">Return code</span></span>                                                                                         | <span data-ttu-id="25ca5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="25ca5-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="25ca5-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="25ca5-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="25ca5-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="25ca5-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="25ca5-120"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="25ca5-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="25ca5-121">Недопустимый профиль.</span><span class="sxs-lookup"><span data-stu-id="25ca5-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="25ca5-122"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="25ca5-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="25ca5-123">Граф фильтра остановлен.</span><span class="sxs-lookup"><span data-stu-id="25ca5-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25ca5-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25ca5-124">Remarks</span></span>

<span data-ttu-id="25ca5-125">Этот метод устарел, так как в нем предполагается наличие профилей пакета SDK для формата Windows Media версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="25ca5-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="25ca5-126">Чтобы настроить фильтр для профилей версии 7,0 и более поздних, используйте [**иконфигасфвритер:: конфигурефилтерусингпрофиле**](iconfigasfwriter-configurefilterusingprofile.md) или [**Иконфигасфвритер:: конфигурефилтерусингпрофилегуид**](iconfigasfwriter-configurefilterusingprofileguid.md).</span><span class="sxs-lookup"><span data-stu-id="25ca5-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="25ca5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25ca5-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="25ca5-128">[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="25ca5-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

