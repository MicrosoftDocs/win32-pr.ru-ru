---
description: Загружает библиотеку DLL монитора.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: Функция Онлоадингдлл (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673361"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="988bb-103">Функция Онлоадингдлл</span><span class="sxs-lookup"><span data-stu-id="988bb-103">OnLoadingDLL function</span></span>

<span data-ttu-id="988bb-104">Функция **онлоадингдлл** ЗАГРУЖАЕТ библиотеку DLL монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="988bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="988bb-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="988bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="988bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988bb-107">*хфилтерблоб* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="988bb-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-108">Большой двоичный объект, используемый МКСВК для сопоставления монитора с доступными сетевыми картами.</span><span class="sxs-lookup"><span data-stu-id="988bb-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="988bb-109">Этот параметр всегда содержит запрос для интерфейса [ИРТК](irtc.md) , поэтому большинству мониторов не нужно добавлять записи в большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="988bb-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="988bb-110">Однако пользовательский монитор может добавлять дополнительные критерии фильтрации (например, тип MAC должен быть Ethernet).</span><span class="sxs-lookup"><span data-stu-id="988bb-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="988bb-111">*пкреатефлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="988bb-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-112">Флаги, указывающие, как МКСВК управляет созданием монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="988bb-113">Этот параметр должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="988bb-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="988bb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="988bb-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="988bb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="988bb-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="988bb-116"><dt>**\_Создание MCS \_ \_ по одной \_ сетевой плате**</dt></span><span class="sxs-lookup"><span data-stu-id="988bb-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="988bb-117">МКСВК гарантирует, что для каждой сетевой карты существует только один экземпляр этого монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="988bb-118">Второй экземпляр может быть создан только в том случае, если первый из них уничтожается.</span><span class="sxs-lookup"><span data-stu-id="988bb-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="988bb-119"><dt>**\_Создание \_ КОНФИГУРАЦИй MCS \_ по \_ умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="988bb-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="988bb-120">Если у монитора есть внутренняя конфигурация по умолчанию, МКСВК не требует от пользователя настройки монитора до создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="988bb-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="988bb-121">*ппдефаултнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="988bb-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-122">Указатель на указатель на адрес имени монитора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="988bb-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="988bb-123">При создании экземпляров монитора МКСВК использует имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="988bb-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="988bb-124">Например, если имя по умолчанию — "монитор маршрутизатора", первый экземпляр монитора будет "монитор маршрутизатора 1", второй — "RouterMonitor2" и т. д.</span><span class="sxs-lookup"><span data-stu-id="988bb-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="988bb-125">Если возвращается **значение NULL** , мксвк использует имя библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="988bb-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="988bb-126">*ппдескриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="988bb-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-127">Указатель на указатель на адрес описания монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="988bb-128">Описание передается средству управления монитором, которое использует описание для указания пользователю о том, что монитор существует.</span><span class="sxs-lookup"><span data-stu-id="988bb-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="988bb-129">Этот параметр может возвращать **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="988bb-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="988bb-130">*ппдефаултскрипт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="988bb-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-131">Указатель на указатель на адрес скрипта HTML-формы по умолчанию, используемого для настройки монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="988bb-132">Несмотря на то, что экземпляры монитора могут изменять собственный сценарий, большинство мониторов просто загружают сценарий один раз из файла.</span><span class="sxs-lookup"><span data-stu-id="988bb-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="988bb-133">Значение *ппдефаултскрипт* может быть **равно NULL**. Тем не менее, либо монитор не может быть настроен извне, либо должен предоставить скрипт позже.</span><span class="sxs-lookup"><span data-stu-id="988bb-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="988bb-134">В этом случае более эффективно указать скрипт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="988bb-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="988bb-135">*ппдефаултконфиг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="988bb-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="988bb-136">Адрес строки по умолчанию, используемой для настройки монитора при его создании.</span><span class="sxs-lookup"><span data-stu-id="988bb-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="988bb-137">Этому параметру можно присвоить **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="988bb-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988bb-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="988bb-138">Return value</span></span>

<span data-ttu-id="988bb-139">Если функция выполнена успешно, возвращается значение S ОК, что совпадает с параметром \_ "ошибка".</span><span class="sxs-lookup"><span data-stu-id="988bb-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="988bb-140">Если функция завершилась неудачно, МКСВК пропускает указанный монитор из всех списков; После этого невозможно создать монитор этого типа.</span><span class="sxs-lookup"><span data-stu-id="988bb-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="988bb-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="988bb-141">Remarks</span></span>

<span data-ttu-id="988bb-142">Функция **онлоадингдлл** вызывается мксвк при первой загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="988bb-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="988bb-143">Затем библиотека DLL предоставляет значения по умолчанию, которые будут использоваться МКСВК при создании экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="988bb-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="988bb-144">Монитору необходимо выделить всю необходимую память для строк, возвращаемых в МКСВК.</span><span class="sxs-lookup"><span data-stu-id="988bb-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="988bb-145">При возврате МКСВК создает копии всех строк и не пытается освободить возвращаемые строки.</span><span class="sxs-lookup"><span data-stu-id="988bb-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="988bb-146">Монитор должен использовать вспомогательные функции больших двоичных объектов для изменения фильтра BLOB.</span><span class="sxs-lookup"><span data-stu-id="988bb-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="988bb-147">Требования</span><span class="sxs-lookup"><span data-stu-id="988bb-147">Requirements</span></span>



| <span data-ttu-id="988bb-148">Требование</span><span class="sxs-lookup"><span data-stu-id="988bb-148">Requirement</span></span> | <span data-ttu-id="988bb-149">Значение</span><span class="sxs-lookup"><span data-stu-id="988bb-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="988bb-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="988bb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="988bb-151">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="988bb-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="988bb-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="988bb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="988bb-153">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="988bb-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="988bb-154">Заголовок</span><span class="sxs-lookup"><span data-stu-id="988bb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="988bb-155"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="988bb-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




