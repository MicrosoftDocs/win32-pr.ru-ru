---
description: Указывает список строк в Юникоде, представляющих возможности устройства, необходимые для преобразования датчика.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Атрибут MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154635"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="c272b-103">\_ \_ Атрибут требуемых \_ возможностей MF девицестреам</span><span class="sxs-lookup"><span data-stu-id="c272b-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="c272b-104">Указывает список строк в Юникоде, представляющих возможности устройства, необходимые для преобразования датчика.</span><span class="sxs-lookup"><span data-stu-id="c272b-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="c272b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c272b-105">Data type</span></span>

<span data-ttu-id="c272b-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c272b-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="c272b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c272b-107">Remarks</span></span>

<span data-ttu-id="c272b-108">Этот атрибут является необязательным и необходим только в том случае, если преобразование датчика обращается к защищенному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="c272b-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="c272b-109">Значение должно представлять собой разделенный точками с запятой список строковых токенов, определенных в [_ *девицекапабилити* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span><span class="sxs-lookup"><span data-stu-id="c272b-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="c272b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c272b-110">Requirements</span></span>



| <span data-ttu-id="c272b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c272b-111">Requirement</span></span> | <span data-ttu-id="c272b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c272b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c272b-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c272b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c272b-114">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="c272b-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c272b-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c272b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c272b-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c272b-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c272b-117">Header</span><span class="sxs-lookup"><span data-stu-id="c272b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c272b-118"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c272b-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
