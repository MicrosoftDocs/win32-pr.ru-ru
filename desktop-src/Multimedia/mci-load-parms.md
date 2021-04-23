---
title: Структура MCI_LOAD_PARMS (Ммсистем. h)
description: '\_ \_ Структура ПАРМС нагрузки MCI содержит имя файла для загрузки \_ команды MCI Load.'
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- MCI_LOAD_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803359"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="51de1-104">\_ \_ Структура ПАРМС загрузки MCI</span><span class="sxs-lookup"><span data-stu-id="51de1-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="51de1-105">Структура **\_ \_ пармс нагрузки MCI** содержит имя файла для загрузки команды [**MCI \_ Load**](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="51de1-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="51de1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51de1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="51de1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="51de1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="51de1-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="51de1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="51de1-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="51de1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="51de1-110">**лпфиленаме**</span><span class="sxs-lookup"><span data-stu-id="51de1-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="51de1-111">Имя загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="51de1-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51de1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51de1-112">Remarks</span></span>

<span data-ttu-id="51de1-113">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="51de1-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="51de1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="51de1-114">Requirements</span></span>



| <span data-ttu-id="51de1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="51de1-115">Requirement</span></span> | <span data-ttu-id="51de1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="51de1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51de1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51de1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="51de1-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51de1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="51de1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51de1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="51de1-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51de1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51de1-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51de1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="51de1-122"><dt>Ммсистем. h</dt></span><span class="sxs-lookup"><span data-stu-id="51de1-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51de1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51de1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51de1-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="51de1-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="51de1-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="51de1-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="51de1-126">**\_Загрузка MCI**</span><span class="sxs-lookup"><span data-stu-id="51de1-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="51de1-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="51de1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

