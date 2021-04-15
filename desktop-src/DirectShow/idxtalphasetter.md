---
description: Интерфейс Идксталфасеттер задает свойства для действия альфа-установки. Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации воздействия на альфа-метод задания.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Интерфейс Идксталфасеттер (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675880"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="97cdb-103">Интерфейс Идксталфасеттер</span><span class="sxs-lookup"><span data-stu-id="97cdb-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="97cdb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="97cdb-104">\[Deprecated.</span></span> <span data-ttu-id="97cdb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="97cdb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="97cdb-106">`IDxtAlphaSetter`Интерфейс задает свойства для действия [альфа-установки](alpha-setter-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="97cdb-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="97cdb-107">Этот интерфейс внутренне используется службами редактирования DirectShow (DES) при визуализации воздействия на альфа-метод задания.</span><span class="sxs-lookup"><span data-stu-id="97cdb-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="97cdb-108">Приложениям DES не требуется использовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="97cdb-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="97cdb-109">Чтобы задать свойства для перехода в DES, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="97cdb-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="97cdb-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="97cdb-110">Members</span></span>

<span data-ttu-id="97cdb-111">Интерфейс **идксталфасеттер** наследует от **идксеффект**.</span><span class="sxs-lookup"><span data-stu-id="97cdb-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="97cdb-112">**Идксталфасеттер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97cdb-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="97cdb-113">Методы</span><span class="sxs-lookup"><span data-stu-id="97cdb-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97cdb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="97cdb-114">Methods</span></span>

<span data-ttu-id="97cdb-115">Интерфейс **идксталфасеттер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="97cdb-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="97cdb-116">Метод</span><span class="sxs-lookup"><span data-stu-id="97cdb-116">Method</span></span>                                                  | <span data-ttu-id="97cdb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="97cdb-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="97cdb-118">**получение \_ альфа-канала**</span><span class="sxs-lookup"><span data-stu-id="97cdb-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="97cdb-119">Извлекает альфа-значение для всего изображения.</span><span class="sxs-lookup"><span data-stu-id="97cdb-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="97cdb-120">**получить \_ алфарамп**</span><span class="sxs-lookup"><span data-stu-id="97cdb-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="97cdb-121">Извлекает свойство альфа-пандуса.</span><span class="sxs-lookup"><span data-stu-id="97cdb-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="97cdb-122">**разместить \_ альфа-канал**</span><span class="sxs-lookup"><span data-stu-id="97cdb-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="97cdb-123">Задает альфа-значение для всего изображения.</span><span class="sxs-lookup"><span data-stu-id="97cdb-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="97cdb-124">**разместить \_ алфарамп**</span><span class="sxs-lookup"><span data-stu-id="97cdb-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="97cdb-125">Указывает свойство пандус альфа.</span><span class="sxs-lookup"><span data-stu-id="97cdb-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="97cdb-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97cdb-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="97cdb-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="97cdb-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="97cdb-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="97cdb-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="97cdb-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="97cdb-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97cdb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="97cdb-130">Requirements</span></span>



| <span data-ttu-id="97cdb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="97cdb-131">Requirement</span></span> | <span data-ttu-id="97cdb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="97cdb-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97cdb-133">Header</span><span class="sxs-lookup"><span data-stu-id="97cdb-133">Header</span></span><br/>  | <dl> <span data-ttu-id="97cdb-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="97cdb-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="97cdb-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97cdb-135">Library</span></span><br/> | <dl> <span data-ttu-id="97cdb-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97cdb-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




