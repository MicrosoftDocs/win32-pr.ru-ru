---
description: Указывает тип учетных данных, используемых для проверки подлинности.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Элемент Аусмоде (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683338"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="e7c30-103">Элемент Аусмоде (OneX)</span><span class="sxs-lookup"><span data-stu-id="e7c30-103">authMode (OneX) Element</span></span>

<span data-ttu-id="e7c30-104">Элемент Аусмоде (OneX) указывает тип учетных данных, используемых для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e7c30-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="e7c30-105">В следующей таблице описаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="e7c30-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="e7c30-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e7c30-106">Value</span></span>         | <span data-ttu-id="e7c30-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e7c30-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c30-108">мачинеорусер</span><span class="sxs-lookup"><span data-stu-id="e7c30-108">machineOrUser</span></span> | <span data-ttu-id="e7c30-109">Используйте учетные данные компьютера или пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7c30-109">Use machine or user credentials.</span></span> <span data-ttu-id="e7c30-110">При входе пользователя в систему для проверки подлинности используются учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7c30-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="e7c30-111">Если пользователь не вошел в систему, используются учетные данные компьютера.</span><span class="sxs-lookup"><span data-stu-id="e7c30-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="e7c30-112">компьютер</span><span class="sxs-lookup"><span data-stu-id="e7c30-112">machine</span></span>       | <span data-ttu-id="e7c30-113">Использовать только учетные данные компьютера.</span><span class="sxs-lookup"><span data-stu-id="e7c30-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="e7c30-114">пользователь</span><span class="sxs-lookup"><span data-stu-id="e7c30-114">user</span></span>          | <span data-ttu-id="e7c30-115">Используйте только учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7c30-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="e7c30-116">guest</span><span class="sxs-lookup"><span data-stu-id="e7c30-116">guest</span></span>         | <span data-ttu-id="e7c30-117">Используйте только гостевые (пустые) учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e7c30-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="e7c30-118">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e7c30-118">This element is optional.</span></span> <span data-ttu-id="e7c30-119">Если Аусмоде не указан в профиле, `machineOrUser` используется значение.</span><span class="sxs-lookup"><span data-stu-id="e7c30-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="e7c30-120">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Этот элемент будет пропущен, если он есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="e7c30-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e7c30-121">Элемент **аусмоде** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e7c30-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c30-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7c30-122">Remarks</span></span>

<span data-ttu-id="e7c30-123">Этот параметр можно задать в командной строке с помощью команды **netsh wlan set профилепараметер** .</span><span class="sxs-lookup"><span data-stu-id="e7c30-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="e7c30-124">Дополнительные сведения см. в разделе [команды Netsh для беспроводной локальной сети (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="e7c30-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7c30-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e7c30-125">Requirements</span></span>



| <span data-ttu-id="e7c30-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e7c30-126">Requirement</span></span> | <span data-ttu-id="e7c30-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e7c30-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7c30-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7c30-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c30-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7c30-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7c30-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7c30-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c30-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7c30-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7c30-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7c30-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7c30-133">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="e7c30-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e7c30-134">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="e7c30-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="e7c30-135">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="e7c30-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e7c30-136">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="e7c30-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
