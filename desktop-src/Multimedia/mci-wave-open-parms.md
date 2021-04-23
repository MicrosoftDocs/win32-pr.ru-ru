---
title: Структура MCI_WAVE_OPEN_PARMS (МЦиапи. h)
description: Структура MCI \_ Wave \_ Open \_ пармс содержит сведения о команде MCI \_ Open для устройств аудио-Audio.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- MCI_WAVE_OPEN_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a4107c6283edab1ffeaf18297e2898a8b17761
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672767"
---
# <a name="mci_wave_open_parms-structure"></a><span data-ttu-id="9ba0e-104">\_ \_ \_ Структура пармс для звукозаписи MCI</span><span class="sxs-lookup"><span data-stu-id="9ba0e-104">MCI\_WAVE\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="9ba0e-105">Структура **MCI \_ Wave \_ Open \_ пармс** содержит сведения о команде [**MCI \_ Open**](mci-open.md) для устройств аудио-Audio.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-105">The **MCI\_WAVE\_OPEN\_PARMS** structure contains information for [**MCI\_OPEN**](mci-open.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ba0e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ba0e-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="9ba0e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="9ba0e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ba0e-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9ba0e-110">**вдевицеид**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-111">Идентификатор, возвращенный приложению.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-111">Indentifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="9ba0e-112">**лпстрдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-113">Имя или идентификатор константы типа устройства.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="9ba0e-114">(Обычно имя устройства берется из реестра или файла SYSTEM.INI.) Этот элемент может быть одним из значений, перечисленных в [типах устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="9ba0e-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ba0e-115">**лпстрелементнаме**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-116">Имя элемента устройства (обычно путь).</span><span class="sxs-lookup"><span data-stu-id="9ba0e-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="9ba0e-117">**лпстралиас**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-118">Необязательный псевдоним устройства.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="9ba0e-119">**двбуфферсекондс**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-119">**dwBufferSeconds**</span></span>
</dt> <dd>

<span data-ttu-id="9ba0e-120">Длина буфера в секундах.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-120">Buffer length, in seconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ba0e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ba0e-121">Remarks</span></span>

<span data-ttu-id="9ba0e-122">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="9ba0e-122">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="9ba0e-123">Если вы не используете расширенные элементы данных, можно использовать структуру [**MCI \_ Open \_ пармс**](mci-open-parms.md) , а не звукозапись **MCI \_ \_ Open \_ пармс** .</span><span class="sxs-lookup"><span data-stu-id="9ba0e-123">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure instead of **MCI\_WAVE\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba0e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9ba0e-124">Requirements</span></span>



| <span data-ttu-id="9ba0e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9ba0e-125">Requirement</span></span> | <span data-ttu-id="9ba0e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9ba0e-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba0e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ba0e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba0e-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ba0e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ba0e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ba0e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba0e-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9ba0e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ba0e-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9ba0e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba0e-132"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba0e-132"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba0e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ba0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ba0e-134">**MCI**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-134">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9ba0e-135">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-135">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9ba0e-136">**MCI \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-136">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="9ba0e-137">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba0e-137">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ba0e-138">**MCI \_ Open \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="9ba0e-138">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> </dl>

 

