---
description: Структура ПРОВИДОР \_ info \_ 1 определяет поставщика печати.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Структура PROVIDOR_INFO_1 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347485"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="61ab5-103">\_Структура провидор info \_ 1</span><span class="sxs-lookup"><span data-stu-id="61ab5-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="61ab5-104">Структура **провидор \_ info \_ 1** определяет поставщика печати.</span><span class="sxs-lookup"><span data-stu-id="61ab5-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ab5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61ab5-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="61ab5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="61ab5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="61ab5-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="61ab5-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="61ab5-108">Указатель на строку, завершающуюся нулем, которая является именем поставщика печати.</span><span class="sxs-lookup"><span data-stu-id="61ab5-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="61ab5-109">**пенвиронмент**</span><span class="sxs-lookup"><span data-stu-id="61ab5-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="61ab5-110">Указатель на строку среды, заканчивающуюся нулем, указывающую среду, которую библиотека динамической компоновки (DLL) поставщика поддерживает для запуска.</span><span class="sxs-lookup"><span data-stu-id="61ab5-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="61ab5-111">**пдллнаме**</span><span class="sxs-lookup"><span data-stu-id="61ab5-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="61ab5-112">Указатель на строку, завершающуюся нулем, которая является именем файла provider. dll.</span><span class="sxs-lookup"><span data-stu-id="61ab5-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61ab5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="61ab5-113">Requirements</span></span>



| <span data-ttu-id="61ab5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="61ab5-114">Requirement</span></span> | <span data-ttu-id="61ab5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="61ab5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61ab5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61ab5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61ab5-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61ab5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="61ab5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61ab5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61ab5-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61ab5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="61ab5-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="61ab5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61ab5-121"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61ab5-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="61ab5-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="61ab5-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="61ab5-123">**\_ \_ Сведения о провидор \_ 1W** (Юникод) и **\_ провидор \_ info \_ 1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="61ab5-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="61ab5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61ab5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61ab5-125">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="61ab5-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="61ab5-126">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="61ab5-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="61ab5-127">**аддпринтпровидор**</span><span class="sxs-lookup"><span data-stu-id="61ab5-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




