---
title: Структура MCI_OVLY_OPEN_PARMS (Ммсистем. h)
description: '\_ \_ Структура овли Open ПАРМС в MCI \_ содержит сведения о команде MCI \_ Open для устройств наложения видео.'
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488988"
---
# <a name="mci_ovly_open_parms-structure"></a><span data-ttu-id="e8c4f-104">\_Структура MCI овли \_ Open \_ пармс</span><span class="sxs-lookup"><span data-stu-id="e8c4f-104">MCI\_OVLY\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="e8c4f-105">Структура **\_ овли \_ Open \_ пармс в MCI** содержит сведения о команде [**MCI \_ Open**](mci-open.md) для устройств наложения видео.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-105">The **MCI\_OVLY\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c4f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8c4f-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="e8c4f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="e8c4f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8c4f-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-110">**вдевицеид**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-111">Идентификатор, возвращенный приложению.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-112">**лпстрдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-113">Имя или идентификатор константы типа устройства.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="e8c4f-114">(Обычно имя устройства берется из реестра или файла SYSTEM.INI.) Если этот член является константой, это может быть одно из значений, перечисленных в [типах устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="e8c4f-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-115">**лпстрелементнаме**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-116">Имя элемента устройства (обычно путь).</span><span class="sxs-lookup"><span data-stu-id="e8c4f-116">Device element name (usually a path).</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-117">**лпстралиас**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-118">Необязательный псевдоним устройства.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-118">Optional device alias.</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-119">**двстиле**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-119">**dwStyle**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-120">Стиль окна.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-120">Window style.</span></span>

</dd> <dt>

<span data-ttu-id="e8c4f-121">**хвндпарент**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-121">**hWndParent**</span></span>
</dt> <dd>

<span data-ttu-id="e8c4f-122">Маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-122">Handle to parent window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8c4f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c4f-123">Remarks</span></span>

<span data-ttu-id="e8c4f-124">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-124">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="e8c4f-125">Структуру [**\_ \_ пармс для MCI**](mci-open-parms.md) можно использовать вместо **MCI \_ овли \_ Open \_ пармс** , если вы не используете расширенные элементы данных.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-125">You can use the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure in place of **MCI\_OVLY\_OPEN\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c4f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c4f-126">Requirements</span></span>



| <span data-ttu-id="e8c4f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e8c4f-127">Requirement</span></span> | <span data-ttu-id="e8c4f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e8c4f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c4f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8c4f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c4f-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8c4f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e8c4f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8c4f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c4f-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8c4f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8c4f-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8c4f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8c4f-134"><dt>Ммсистем. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c4f-134"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c4f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8c4f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c4f-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e8c4f-137">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="e8c4f-138">**MCI \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-138">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

[<span data-ttu-id="e8c4f-139">**MCI \_ Open \_ пармс**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-139">**MCI\_OPEN\_PARMS**</span></span>](mci-open-parms.md)
</dt> <dt>

<span data-ttu-id="e8c4f-140">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8c4f-140">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

