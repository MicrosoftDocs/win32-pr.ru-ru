---
title: Идевицеброкер Опендевицефроминтерфацепас, метод
description: Пытается открыть экземпляр интерфейса устройства от имени клиента. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Интерфейс API брокера доступа устройства Опендевицефроминтерфацепас
- API брокера доступа устройства Опендевицефроминтерфацепас, интерфейс Идевицеброкер
- API брокера доступа устройства интерфейса Идевицеброкер, метод Опендевицефроминтерфацепас
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412459"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="18127-107">Метод Идевицеброкер:: Опендевицефроминтерфацепас</span><span class="sxs-lookup"><span data-stu-id="18127-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="18127-108">Эти интерфейсы не поддерживаются, и их не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="18127-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="18127-109">Вместо этого используйте API-интерфейсы в [справочнике по программированию API для доступа к устройствам](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="18127-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="18127-110">Пытается открыть экземпляр интерфейса устройства от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="18127-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="18127-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span><span class="sxs-lookup"><span data-stu-id="18127-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="18127-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18127-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="18127-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="18127-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18127-114">*псздевицеинтерфацепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18127-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18127-115">Открываемый экземпляр интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="18127-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="18127-116">*десиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18127-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18127-117">Требуемый доступ, передаваемый в Open.</span><span class="sxs-lookup"><span data-stu-id="18127-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="18127-118">*шаремоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18127-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18127-119">Режим предоставления общего доступа, который должен быть передан в открытие.</span><span class="sxs-lookup"><span data-stu-id="18127-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="18127-120">*флагсандаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18127-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18127-121">Флаги и атрибуты, которые должны быть переданы для открытия.</span><span class="sxs-lookup"><span data-stu-id="18127-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="18127-122">*\* фдевице* \[\]</span><span class="sxs-lookup"><span data-stu-id="18127-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18127-123">Результирующий обработчик, если открыт успешно.</span><span class="sxs-lookup"><span data-stu-id="18127-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18127-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18127-124">Return value</span></span>

<span data-ttu-id="18127-125">Если эта функция завершается с ошибкой, возвращается S_OK.</span><span class="sxs-lookup"><span data-stu-id="18127-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="18127-126">В противном случае возвращается код ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="18127-126">Otherwise, it returns an HRESULT error code.</span></span>
