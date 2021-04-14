---
description: Интерфейс Идксткэй задает свойства для перехода по ключу. Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации ключевых переходов.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Интерфейс Идксткэй (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675615"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="1cb26-103">Интерфейс Идксткэй</span><span class="sxs-lookup"><span data-stu-id="1cb26-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="1cb26-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1cb26-104">\[Deprecated.</span></span> <span data-ttu-id="1cb26-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1cb26-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1cb26-106">`IDxtKey`Интерфейс задает свойства для перехода по [ключу](key-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb26-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="1cb26-107">Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации ключевых переходов.</span><span class="sxs-lookup"><span data-stu-id="1cb26-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="1cb26-108">Приложениям DES не требуется использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1cb26-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="1cb26-109">Чтобы задать свойства для перехода в DES, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb26-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="1cb26-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="1cb26-110">Members</span></span>

<span data-ttu-id="1cb26-111">Интерфейс **идксткэй** наследует от **идксеффект**.</span><span class="sxs-lookup"><span data-stu-id="1cb26-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="1cb26-112">**Идксткэй** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1cb26-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="1cb26-113">Методы</span><span class="sxs-lookup"><span data-stu-id="1cb26-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1cb26-114">Методы</span><span class="sxs-lookup"><span data-stu-id="1cb26-114">Methods</span></span>

<span data-ttu-id="1cb26-115">Интерфейс **идксткэй** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1cb26-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="1cb26-116">Метод</span><span class="sxs-lookup"><span data-stu-id="1cb26-116">Method</span></span>                                            | <span data-ttu-id="1cb26-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1cb26-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cb26-118">**получить \_ оттенок**</span><span class="sxs-lookup"><span data-stu-id="1cb26-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="1cb26-119">Возвращает значение оттенка, по которому следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="1cb26-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="1cb26-120">**получить \_ инверсию**</span><span class="sxs-lookup"><span data-stu-id="1cb26-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="1cb26-121">Получает логическое значение, указывающее, выполняется ли обратная операция с ключом.</span><span class="sxs-lookup"><span data-stu-id="1cb26-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="1cb26-122">**получить \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="1cb26-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="1cb26-123">Возвращает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="1cb26-124">**получить \_ светимость**</span><span class="sxs-lookup"><span data-stu-id="1cb26-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="1cb26-125">Извлекает значение светимости для ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="1cb26-126">**получить \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="1cb26-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="1cb26-127">Извлекает цвет RGB, по которому следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="1cb26-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="1cb26-128">**получить \_ подобие**</span><span class="sxs-lookup"><span data-stu-id="1cb26-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="1cb26-129">Извлекает диапазон цветовых данных, которые становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="1cb26-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="1cb26-130">**вставить \_ оттенок**</span><span class="sxs-lookup"><span data-stu-id="1cb26-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="1cb26-131">Задает значение оттенка ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="1cb26-132">**вернуть \_ инверсию**</span><span class="sxs-lookup"><span data-stu-id="1cb26-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="1cb26-133">Указывает, выполняется ли обратная операция с ключом.</span><span class="sxs-lookup"><span data-stu-id="1cb26-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="1cb26-134">**вставить \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="1cb26-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="1cb26-135">Указывает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="1cb26-136">**Поставьте \_ светимость**</span><span class="sxs-lookup"><span data-stu-id="1cb26-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="1cb26-137">Задает значение светимости для ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="1cb26-138">**перевести \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="1cb26-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="1cb26-139">Задает цвет RGB для ключа.</span><span class="sxs-lookup"><span data-stu-id="1cb26-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="1cb26-140">**разместить \_ подобие**</span><span class="sxs-lookup"><span data-stu-id="1cb26-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="1cb26-141">Указывает диапазон цветовых данных, которые становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="1cb26-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="1cb26-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cb26-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1cb26-143">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1cb26-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1cb26-144">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1cb26-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1cb26-145">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1cb26-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1cb26-146">Требования</span><span class="sxs-lookup"><span data-stu-id="1cb26-146">Requirements</span></span>



| <span data-ttu-id="1cb26-147">Требование</span><span class="sxs-lookup"><span data-stu-id="1cb26-147">Requirement</span></span> | <span data-ttu-id="1cb26-148">Значение</span><span class="sxs-lookup"><span data-stu-id="1cb26-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb26-149">Header</span><span class="sxs-lookup"><span data-stu-id="1cb26-149">Header</span></span><br/>  | <dl> <span data-ttu-id="1cb26-150"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb26-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1cb26-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1cb26-151">Library</span></span><br/> | <dl> <span data-ttu-id="1cb26-152"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cb26-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




