---
title: Структура MCI_SEEK_PARMS (МЦиапи. h)
description: '\_ \_ Структура ПАРМС поиска MCI содержит сведения о размещении для \_ команды MCI Seek.'
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- MCI_SEEK_PARMS структура мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801516"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="7e1f1-104">\_ \_ Структура ПАРМС поиска MCI</span><span class="sxs-lookup"><span data-stu-id="7e1f1-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="7e1f1-105">Структура **\_ \_ пармс поиска MCI** содержит сведения о размещении для команды [**MCI \_ Seek**](mci-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="7e1f1-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1f1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e1f1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="7e1f1-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7e1f1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e1f1-108">**двкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7e1f1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="7e1f1-109">Слово нижнего порядка задает маркер окна, используемый для \_ флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="7e1f1-110">**двто**</span><span class="sxs-lookup"><span data-stu-id="7e1f1-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="7e1f1-111">Положение для поиска.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e1f1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e1f1-112">Remarks</span></span>

<span data-ttu-id="7e1f1-113">При назначении данных членам этой структуры установите соответствующие флаги в параметре *фдвкомманд* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы проверить элементы.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e1f1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7e1f1-114">Requirements</span></span>



| <span data-ttu-id="7e1f1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7e1f1-115">Requirement</span></span> | <span data-ttu-id="7e1f1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7e1f1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e1f1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e1f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e1f1-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7e1f1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7e1f1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e1f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e1f1-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7e1f1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7e1f1-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7e1f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e1f1-122"><dt>МЦиапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e1f1-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e1f1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e1f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e1f1-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="7e1f1-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7e1f1-125">**Структуры MCI**</span><span class="sxs-lookup"><span data-stu-id="7e1f1-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="7e1f1-126">**\_Поиск MCI**</span><span class="sxs-lookup"><span data-stu-id="7e1f1-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="7e1f1-127">[**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e1f1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

