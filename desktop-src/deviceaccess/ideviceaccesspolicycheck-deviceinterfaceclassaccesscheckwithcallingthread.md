---
title: Идевицеакцессполицичекк Девицеинтерфацеклассакцессчекквискаллингсреад, метод
description: Этот API определит, имеет ли маркер текущего контекста доступ к указанному классу интерфейса устройства. IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Интерфейс API брокера доступа устройства Девицеинтерфацеклассакцессчекквискаллингсреад
- API брокера доступа устройства Девицеинтерфацеклассакцессчекквискаллингсреад, интерфейс Идевицеакцессполицичекк
- API брокера доступа устройства интерфейса Идевицеакцессполицичекк, метод Девицеинтерфацеклассакцессчекквискаллингсреад
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105719101"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="147a8-107">Идевицеакцессполицичекк: метод:D Евицеинтерфацеклассакцессчекквискаллингсреад</span><span class="sxs-lookup"><span data-stu-id="147a8-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="147a8-108">Эти интерфейсы не поддерживаются, и их не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="147a8-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="147a8-109">Вместо этого используйте API-интерфейсы в [справочнике по программированию API для доступа к устройствам](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="147a8-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="147a8-110">Этот API определит, имеет ли маркер текущего контекста доступ к указанному классу интерфейса устройства.</span><span class="sxs-lookup"><span data-stu-id="147a8-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="147a8-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span><span class="sxs-lookup"><span data-stu-id="147a8-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="147a8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="147a8-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="147a8-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="147a8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="147a8-114">*псздевицеинтерфацеклассгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="147a8-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="147a8-115">Идентификатор GUID класса интерфейса устройства, для которого необходимо проверить доступ.</span><span class="sxs-lookup"><span data-stu-id="147a8-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="147a8-116">*двклиентсреадид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="147a8-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="147a8-117">Идентификатор клиентского потока, в котором при необходимости должен отображаться любой связанный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="147a8-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="147a8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="147a8-118">Return value</span></span>

<span data-ttu-id="147a8-119">Если эта функция завершается с ошибкой, возвращается S_OK.</span><span class="sxs-lookup"><span data-stu-id="147a8-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="147a8-120">В противном случае возвращается код ошибки HRESULT.</span><span class="sxs-lookup"><span data-stu-id="147a8-120">Otherwise, it returns an HRESULT error code.</span></span>
