---
title: Ивмпсеттингс setMode, метод
description: Метод setMode устанавливает активный или неактивный режим цикла или случайного режима.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setMode метод Windows Media Player
- setMode метод проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, метод setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717783"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="7e894-106">Метод Ивмпсеттингс:: setMode</span><span class="sxs-lookup"><span data-stu-id="7e894-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="7e894-107">Метод **setMode** устанавливает активный или неактивный режим цикла или случайного режима.</span><span class="sxs-lookup"><span data-stu-id="7e894-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e894-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e894-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="7e894-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e894-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e894-110">*бстрмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e894-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e894-111">**Строка System. String** , которая является именем изменяемого режима, содержащего одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7e894-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="7e894-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7e894-112">Value</span></span>      | <span data-ttu-id="7e894-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7e894-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e894-114">ауторевинд</span><span class="sxs-lookup"><span data-stu-id="7e894-114">autoRewind</span></span> | <span data-ttu-id="7e894-115">Дорожки перезапускаются с начала после воспроизведения до конца.</span><span class="sxs-lookup"><span data-stu-id="7e894-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="7e894-116">loop</span><span class="sxs-lookup"><span data-stu-id="7e894-116">loop</span></span>       | <span data-ttu-id="7e894-117">Последовательность дорожек повторяется самим собой.</span><span class="sxs-lookup"><span data-stu-id="7e894-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="7e894-118">шовфраме</span><span class="sxs-lookup"><span data-stu-id="7e894-118">showFrame</span></span>  | <span data-ttu-id="7e894-119">Ближайший ключевой кадр отображается, когда не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="7e894-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="7e894-120">Этот режим не подходит для звуковых дорожек.</span><span class="sxs-lookup"><span data-stu-id="7e894-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="7e894-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="7e894-121">shuffle</span></span>    | <span data-ttu-id="7e894-122">Дорожки воспроизводятся в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="7e894-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="7e894-123">*варфмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e894-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e894-124">Значение **System. Boolean** , указывающее, активен ли новый заданный режим.</span><span class="sxs-lookup"><span data-stu-id="7e894-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e894-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e894-125">Return value</span></span>

<span data-ttu-id="7e894-126">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7e894-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e894-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e894-127">Remarks</span></span>

<span data-ttu-id="7e894-128">Когда активен режим Шовфраме, проигрыватель Windows Media должен получить доступ к содержимому дорожки, чтобы получить кадр видео.</span><span class="sxs-lookup"><span data-stu-id="7e894-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="7e894-129">Используйте этот режим с осторожностью при воспроизведении содержимого, которое не является локальным.</span><span class="sxs-lookup"><span data-stu-id="7e894-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e894-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7e894-130">Requirements</span></span>



| <span data-ttu-id="7e894-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7e894-131">Requirement</span></span> | <span data-ttu-id="7e894-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7e894-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e894-133">Версия</span><span class="sxs-lookup"><span data-stu-id="7e894-133">Version</span></span><br/>   | <span data-ttu-id="7e894-134">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7e894-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7e894-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7e894-135">Namespace</span></span><br/> | <span data-ttu-id="7e894-136">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7e894-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7e894-137">Сборка</span><span class="sxs-lookup"><span data-stu-id="7e894-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e894-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e894-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e894-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e894-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e894-140">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e894-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e894-141">**Ивмпсеттингс. мода (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7e894-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





