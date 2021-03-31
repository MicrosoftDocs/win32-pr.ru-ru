---
description: Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.
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
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263128"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="567d8-103">IWiaUIExtension2: метод:D Евицедиалог</span><span class="sxs-lookup"><span data-stu-id="567d8-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="567d8-104">Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="567d8-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="567d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="567d8-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="567d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="567d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567d8-107">*пдевицедиалогдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="567d8-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="567d8-108">Тип: \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="567d8-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="567d8-109">Указывает на структуру [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) , которая содержит все данные, необходимые для реализации диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="567d8-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567d8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="567d8-110">Return value</span></span>

<span data-ttu-id="567d8-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="567d8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="567d8-112">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="567d8-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="567d8-113">Если пользователь отменяет диалоговое окно, метод возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="567d8-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="567d8-114">Если метод завершается с ошибкой, возвращается соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="567d8-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="567d8-115">В следующей таблице показаны некоторые из возможных кодов состояния возврата.</span><span class="sxs-lookup"><span data-stu-id="567d8-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="567d8-116">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="567d8-116">Error code</span></span>    | <span data-ttu-id="567d8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="567d8-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="567d8-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="567d8-118">E\_INVALIDARG</span></span> | <span data-ttu-id="567d8-119">Параметр Пдевицедиалогдата имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="567d8-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="567d8-120">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="567d8-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="567d8-121">Метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="567d8-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="567d8-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="567d8-122">Remarks</span></span>

<span data-ttu-id="567d8-123">Если вы реализуете интерфейс [**IWiaUIExtension2**](-wia-iwiauiextension2.md) и не хотите заменять системный интерфейс пользователя, этот метод по-прежнему должен быть реализован, но не должен делать ничего больше, чем возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="567d8-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="567d8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="567d8-124">Requirements</span></span>



| <span data-ttu-id="567d8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="567d8-125">Requirement</span></span> | <span data-ttu-id="567d8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="567d8-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="567d8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="567d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="567d8-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="567d8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="567d8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="567d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="567d8-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="567d8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="567d8-131">Header</span><span class="sxs-lookup"><span data-stu-id="567d8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="567d8-132"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="567d8-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




