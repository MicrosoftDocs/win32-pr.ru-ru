---
description: 'IWiaUIExtension2: метод:D Евицедиалог — предоставляет пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.'
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: 'IWiaUIExtension2: метод:D Евицедиалог (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116652"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="54002-103">IWiaUIExtension2: метод:D Евицедиалог</span><span class="sxs-lookup"><span data-stu-id="54002-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="54002-104">Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="54002-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="54002-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54002-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="54002-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54002-107">*пдевицедиалогдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54002-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54002-108">Тип: **PDEVICEDIALOGDATA2 \***</span><span class="sxs-lookup"><span data-stu-id="54002-108">Type: **PDEVICEDIALOGDATA2\***</span></span>

<span data-ttu-id="54002-109">Указывает на структуру [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) , содержащую все данные, необходимые для реализации диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="54002-109">Points to a [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54002-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54002-110">Return value</span></span>

<span data-ttu-id="54002-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="54002-111">Type: **HRESULT**</span></span>

<span data-ttu-id="54002-112">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="54002-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="54002-113">Если пользователь отменяет диалоговое окно, метод возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="54002-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="54002-114">Если метод завершается с ошибкой, возвращается соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="54002-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="54002-115">В следующей таблице показаны некоторые из возможных кодов состояния возврата.</span><span class="sxs-lookup"><span data-stu-id="54002-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="54002-116">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="54002-116">Error code</span></span>    | <span data-ttu-id="54002-117">Описание</span><span class="sxs-lookup"><span data-stu-id="54002-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="54002-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="54002-118">E\_INVALIDARG</span></span> | <span data-ttu-id="54002-119">Параметр Пдевицедиалогдата имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="54002-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="54002-120">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="54002-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="54002-121">Метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="54002-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="54002-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="54002-122">Remarks</span></span>

<span data-ttu-id="54002-123">Если вы реализуете интерфейс [**IWiaUIExtension2**](-wia-iwiauiextension2.md) и не хотите заменять системный интерфейс пользователя, этот метод по-прежнему должен быть реализован, но не должен делать ничего больше, чем возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="54002-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="54002-124">Требования</span><span class="sxs-lookup"><span data-stu-id="54002-124">Requirements</span></span>



| <span data-ttu-id="54002-125">Требование</span><span class="sxs-lookup"><span data-stu-id="54002-125">Requirement</span></span> | <span data-ttu-id="54002-126">Значение</span><span class="sxs-lookup"><span data-stu-id="54002-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54002-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54002-127">Minimum supported client</span></span><br/> | <span data-ttu-id="54002-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54002-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="54002-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54002-129">Minimum supported server</span></span><br/> | <span data-ttu-id="54002-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54002-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54002-131">Header</span><span class="sxs-lookup"><span data-stu-id="54002-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="54002-132"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="54002-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




