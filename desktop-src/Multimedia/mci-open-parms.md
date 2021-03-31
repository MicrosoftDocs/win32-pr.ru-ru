---
title: Структура MCI_OPEN_PARMS (МЦиапи. h)
description: Структура MCI \_ Open \_ пармс содержит сведения для \_ команды MCI Open.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- MCI_OPEN_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135675"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="88e96-104">\_Структура Open \_ ПАРМС для MCI</span><span class="sxs-lookup"><span data-stu-id="88e96-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="88e96-105">Структура **MCI \_ Open \_ пармс** содержит сведения для команды [**MCI \_ Open**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="88e96-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e96-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88e96-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="88e96-107">Члены</span><span class="sxs-lookup"><span data-stu-id="88e96-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="88e96-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="88e96-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="88e96-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="88e96-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="88e96-110">**вдевицеид**</span><span class="sxs-lookup"><span data-stu-id="88e96-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="88e96-111">Идентификатор, возвращенный приложению.</span><span class="sxs-lookup"><span data-stu-id="88e96-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="88e96-112">**лпстрдевицетипе**</span><span class="sxs-lookup"><span data-stu-id="88e96-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="88e96-113">Имя или идентификатор константы типа устройства.</span><span class="sxs-lookup"><span data-stu-id="88e96-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="88e96-114">(Обычно имя устройства берется из реестра или файла SYSTEM.INI.) Если этот член является константой, это может быть одно из значений, перечисленных в [типах устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="88e96-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="88e96-115">**лпстрелементнаме**</span><span class="sxs-lookup"><span data-stu-id="88e96-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="88e96-116">Элемент Device (часто путь).</span><span class="sxs-lookup"><span data-stu-id="88e96-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="88e96-117">**лпстралиас**</span><span class="sxs-lookup"><span data-stu-id="88e96-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="88e96-118">Необязательный псевдоним устройства.</span><span class="sxs-lookup"><span data-stu-id="88e96-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88e96-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88e96-119">Remarks</span></span>

<span data-ttu-id="88e96-120">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="88e96-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e96-121">Требования</span><span class="sxs-lookup"><span data-stu-id="88e96-121">Requirements</span></span>



| <span data-ttu-id="88e96-122">Требование</span><span class="sxs-lookup"><span data-stu-id="88e96-122">Requirement</span></span> | <span data-ttu-id="88e96-123">Значение</span><span class="sxs-lookup"><span data-stu-id="88e96-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88e96-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88e96-124">Minimum supported client</span></span><br/> | <span data-ttu-id="88e96-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88e96-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88e96-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88e96-126">Minimum supported server</span></span><br/> | <span data-ttu-id="88e96-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="88e96-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88e96-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="88e96-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e96-129"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e96-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e96-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88e96-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e96-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="88e96-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="88e96-132">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="88e96-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="88e96-133">**MCI \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="88e96-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="88e96-134">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88e96-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

