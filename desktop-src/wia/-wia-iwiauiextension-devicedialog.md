---
description: 'Ивиауиекстенсион: метод:D Евицедиалог — предоставляет пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.'
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: 'Ивиауиекстенсион: метод:D Евицедиалог (Виадевд. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116712"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="00f73-103">Ивиауиекстенсион: метод:D Евицедиалог</span><span class="sxs-lookup"><span data-stu-id="00f73-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="00f73-104">Предоставляет настраиваемый пользовательский интерфейс, который заменяет стандартный системный интерфейс пользователя.</span><span class="sxs-lookup"><span data-stu-id="00f73-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00f73-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="00f73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00f73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f73-107">*пдевицедиалогдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00f73-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f73-108">Тип: **пдевицедиалогдата \***</span><span class="sxs-lookup"><span data-stu-id="00f73-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="00f73-109">Указывает на структуру [**девицедиалогдата**](-wia-devicedialogdata.md) , содержащую все данные, необходимые для реализации диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="00f73-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f73-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00f73-110">Return value</span></span>

<span data-ttu-id="00f73-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00f73-111">Type: **HRESULT**</span></span>

<span data-ttu-id="00f73-112">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="00f73-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="00f73-113">Если пользователь отменяет диалоговое окно, метод возвращает \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="00f73-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="00f73-114">Если метод не реализован, он возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="00f73-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="00f73-115">Если метод завершается с ошибкой, возвращается стандартный код ошибки COM.</span><span class="sxs-lookup"><span data-stu-id="00f73-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00f73-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="00f73-116">Remarks</span></span>

<span data-ttu-id="00f73-117">Если вы реализуете интерфейс [**ивиауиекстенсион**](-wia-iwiauiextension.md) и не хотите заменять системный интерфейс пользователя, этот метод по-прежнему должен быть реализован, но не должен делать ничего больше, чем возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="00f73-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f73-118">Требования</span><span class="sxs-lookup"><span data-stu-id="00f73-118">Requirements</span></span>



| <span data-ttu-id="00f73-119">Требование</span><span class="sxs-lookup"><span data-stu-id="00f73-119">Requirement</span></span> | <span data-ttu-id="00f73-120">Значение</span><span class="sxs-lookup"><span data-stu-id="00f73-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00f73-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00f73-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00f73-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="00f73-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="00f73-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00f73-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00f73-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00f73-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00f73-125">Header</span><span class="sxs-lookup"><span data-stu-id="00f73-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f73-126"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f73-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




