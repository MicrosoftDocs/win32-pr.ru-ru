---
title: Ивмпсеттингс, метод
description: Метод метода мода возвращает значение, указывающее, активен ли режим "цикл" или "случайный".
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- метод мода проигрыватель Windows Media
- метод onmode проигрыватель Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, методического режима
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717907"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="b9652-106">Метод Ивмпсеттингс:: onmode</span><span class="sxs-lookup"><span data-stu-id="b9652-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="b9652-107">Метод метода **мода** возвращает значение, указывающее, активен ли режим "цикл" или "случайный".</span><span class="sxs-lookup"><span data-stu-id="b9652-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9652-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9652-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="b9652-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9652-110">*бстрмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b9652-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9652-111">**Строка System. String** , которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b9652-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="b9652-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b9652-112">Value</span></span>      | <span data-ttu-id="b9652-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b9652-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9652-114">ауторевинд</span><span class="sxs-lookup"><span data-stu-id="b9652-114">autoRewind</span></span> | <span data-ttu-id="b9652-115">Дорожки перезапускаются с начала после воспроизведения до конца.</span><span class="sxs-lookup"><span data-stu-id="b9652-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="b9652-116">loop</span><span class="sxs-lookup"><span data-stu-id="b9652-116">loop</span></span>       | <span data-ttu-id="b9652-117">Последовательность дорожек повторяется самим собой.</span><span class="sxs-lookup"><span data-stu-id="b9652-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="b9652-118">шовфраме</span><span class="sxs-lookup"><span data-stu-id="b9652-118">showFrame</span></span>  | <span data-ttu-id="b9652-119">Ближайший ключевой кадр отображается, когда не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="b9652-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="b9652-120">Этот режим не подходит для звуковых дорожек.</span><span class="sxs-lookup"><span data-stu-id="b9652-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="b9652-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="b9652-121">shuffle</span></span>    | <span data-ttu-id="b9652-122">Дорожки воспроизводятся в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="b9652-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9652-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9652-123">Return value</span></span>

<span data-ttu-id="b9652-124">Значение **System. Boolean** , указывающее, активен ли заданный режим.</span><span class="sxs-lookup"><span data-stu-id="b9652-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9652-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b9652-125">Requirements</span></span>



| <span data-ttu-id="b9652-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b9652-126">Requirement</span></span> | <span data-ttu-id="b9652-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b9652-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9652-128">Версия</span><span class="sxs-lookup"><span data-stu-id="b9652-128">Version</span></span><br/>   | <span data-ttu-id="b9652-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b9652-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9652-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b9652-130">Namespace</span></span><br/> | <span data-ttu-id="b9652-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b9652-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9652-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="b9652-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9652-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9652-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9652-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9652-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9652-135">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b9652-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9652-136">**Ивмпсеттингс. setMode (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b9652-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





