---
title: Сообщение DRV_OPEN (Ммсистем. h)
description: Указывает драйверу открыть новый экземпляр.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137594"
---
# <a name="drv_open-message"></a><span data-ttu-id="c651e-104">DRV — \_ Открыть сообщение</span><span class="sxs-lookup"><span data-stu-id="c651e-104">DRV\_OPEN message</span></span>

<span data-ttu-id="c651e-105">Указывает драйверу открыть новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c651e-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="c651e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c651e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c651e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*двдриверид*</span><span class="sxs-lookup"><span data-stu-id="c651e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="c651e-108">Идентификатор устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="c651e-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="c651e-109"><span id="hdrvr"></span><span id="HDRVR"></span>*хдрвр*</span><span class="sxs-lookup"><span data-stu-id="c651e-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="c651e-110">Описатель устанавливаемого экземпляра драйвера.</span><span class="sxs-lookup"><span data-stu-id="c651e-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="c651e-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c651e-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c651e-112">Адрес строки расширенных символов, заканчивающейся нулем, которая указывает сведения о конфигурации, используемые для открытия экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c651e-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="c651e-113">Если сведения о конфигурации недоступны, то либо эта строка пустая, либо параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c651e-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c651e-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c651e-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c651e-115">32-разрядные данные, относящиеся к драйверу.</span><span class="sxs-lookup"><span data-stu-id="c651e-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c651e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c651e-116">Return Value</span></span>

<span data-ttu-id="c651e-117">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c651e-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c651e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c651e-118">Remarks</span></span>

<span data-ttu-id="c651e-119">Если драйвер возвращает ненулевое значение, система использует это значение в качестве идентификатора драйвера (параметр *двдриверид* ) в сообщениях, которые он затем отправляет в экземпляр драйвера.</span><span class="sxs-lookup"><span data-stu-id="c651e-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="c651e-120">Драйвер может возвращать любой тип значения в качестве идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c651e-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="c651e-121">Например, некоторые драйверы возвращают адреса памяти, указывающие на сведения, относящиеся к конкретному экземпляру.</span><span class="sxs-lookup"><span data-stu-id="c651e-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="c651e-122">Использование этого метода для указания идентификаторов для экземпляра драйвера предоставляет драйверам доступ к информации во время обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="c651e-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c651e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c651e-123">Requirements</span></span>



| <span data-ttu-id="c651e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c651e-124">Requirement</span></span> | <span data-ttu-id="c651e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c651e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c651e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c651e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c651e-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c651e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c651e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c651e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c651e-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c651e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c651e-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c651e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c651e-131"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c651e-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c651e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c651e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c651e-133">Устанавливаемые драйверы</span><span class="sxs-lookup"><span data-stu-id="c651e-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="c651e-134">Устанавливаемые сообщения драйверов</span><span class="sxs-lookup"><span data-stu-id="c651e-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





