---
description: В \_ структуре "сведения о порте \_ 3" указывается значение состояния порта принтера.
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
title: Структура PORT_INFO_3 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_3
- _PORT_INFO_3A
- _PORT_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 49888ee6410f39745b848bbbf7fd95fa329c6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702207"
---
# <a name="port_info_3-structure"></a><span data-ttu-id="4b104-103">\_Сведения о порте \_ 3 структура</span><span class="sxs-lookup"><span data-stu-id="4b104-103">PORT\_INFO\_3 structure</span></span>

<span data-ttu-id="4b104-104">В структуре " **\_ сведения о порте \_ 3** " указывается значение состояния порта принтера.</span><span class="sxs-lookup"><span data-stu-id="4b104-104">The **PORT\_INFO\_3** structure specifies the status value of a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b104-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b104-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_3 {
  DWORD  dwStatus;
  LPTSTR pszStatus;
  DWORD  dwSeverity;
} PORT_INFO_3, *PPORT_INFO_3;
```



## <a name="members"></a><span data-ttu-id="4b104-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4b104-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b104-107">**Dwstatus устанавливается**</span><span class="sxs-lookup"><span data-stu-id="4b104-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4b104-108">Новое значение состояния порта.</span><span class="sxs-lookup"><span data-stu-id="4b104-108">The new port status value.</span></span> <span data-ttu-id="4b104-109">Это значение используется только в том случае, если элемент **псзстатус** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b104-109">This value is used only if the **pszStatus** member is **NULL**.</span></span>

<span data-ttu-id="4b104-110">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4b104-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="4b104-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4b104-111">Value</span></span>                            | <span data-ttu-id="4b104-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4b104-112">Meaning</span></span>                                             |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="4b104-113">0</span><span class="sxs-lookup"><span data-stu-id="4b104-113">0</span></span>                                | <span data-ttu-id="4b104-114">Очищает состояние порта принтера.</span><span class="sxs-lookup"><span data-stu-id="4b104-114">Clears the printer port status.</span></span>                     |
| <span data-ttu-id="4b104-115">состояние порта в \_ \_ автономном режиме</span><span class="sxs-lookup"><span data-stu-id="4b104-115">PORT\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="4b104-116">Принтер порта отключен.</span><span class="sxs-lookup"><span data-stu-id="4b104-116">The port's printer is offline.</span></span>                      |
| <span data-ttu-id="4b104-117">\_состояние порта \_ \_ Застревание бумаги</span><span class="sxs-lookup"><span data-stu-id="4b104-117">PORT\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="4b104-118">В принтере порта есть Застревание бумаги.</span><span class="sxs-lookup"><span data-stu-id="4b104-118">The port's printer has a paper jam.</span></span>                 |
| <span data-ttu-id="4b104-119">\_Бумага состояния \_ порта \_</span><span class="sxs-lookup"><span data-stu-id="4b104-119">PORT\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="4b104-120">В принтере порта нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="4b104-120">The port's printer is out of paper.</span></span>                 |
| <span data-ttu-id="4b104-121">\_ \_ выходной лоток состояния \_ порта \_ полон</span><span class="sxs-lookup"><span data-stu-id="4b104-121">PORT\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="4b104-122">Выходной лоток принтер'с для порта заполнен.</span><span class="sxs-lookup"><span data-stu-id="4b104-122">The port's printer's output bin is full.</span></span>            |
| <span data-ttu-id="4b104-123">\_проблема с \_ бумагой о состоянии порта \_</span><span class="sxs-lookup"><span data-stu-id="4b104-123">PORT\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="4b104-124">На принтере порта имеется проблема с бумагой.</span><span class="sxs-lookup"><span data-stu-id="4b104-124">The port's printer has a paper problem.</span></span>             |
| <span data-ttu-id="4b104-125">\_состояние порта \_ без \_ тонера</span><span class="sxs-lookup"><span data-stu-id="4b104-125">PORT\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="4b104-126">У принтера порта нет тонера.</span><span class="sxs-lookup"><span data-stu-id="4b104-126">The port's printer is out of toner.</span></span>                 |
| <span data-ttu-id="4b104-127">\_ \_ открыта дверца состояния порта \_</span><span class="sxs-lookup"><span data-stu-id="4b104-127">PORT\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="4b104-128">Открыта дверца принтера порта.</span><span class="sxs-lookup"><span data-stu-id="4b104-128">The door of the port's printer is open.</span></span>             |
| <span data-ttu-id="4b104-129">\_состояние порта \_ \_ вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="4b104-129">PORT\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="4b104-130">Для принтера порта требуется вмешательство пользователя.</span><span class="sxs-lookup"><span data-stu-id="4b104-130">The port's printer requires user intervention.</span></span>      |
| <span data-ttu-id="4b104-131">состояние порта " \_ \_ недостаточно \_ \_ памяти"</span><span class="sxs-lookup"><span data-stu-id="4b104-131">PORT\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="4b104-132">В принтере порта не хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="4b104-132">The port's printer is out of memory.</span></span>                |
| <span data-ttu-id="4b104-133">\_ \_ низкое тонер состояния \_ порта</span><span class="sxs-lookup"><span data-stu-id="4b104-133">PORT\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="4b104-134">На принтере порта не хватает тонера.</span><span class="sxs-lookup"><span data-stu-id="4b104-134">The port's printer is low on toner.</span></span>                 |
| <span data-ttu-id="4b104-135">\_прогрев состояния \_ порта \_</span><span class="sxs-lookup"><span data-stu-id="4b104-135">PORT\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="4b104-136">Принтер порта прогрев.</span><span class="sxs-lookup"><span data-stu-id="4b104-136">The port's printer is warming up.</span></span>                   |
| <span data-ttu-id="4b104-137">состояние порта "Энергосбережение" \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4b104-137">PORT\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="4b104-138">Принтер порта находится в режиме экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="4b104-138">The port's printer is in a power-conservation mode.</span></span> |



 

</dd> <dt>

<span data-ttu-id="4b104-139">**псзстатус**</span><span class="sxs-lookup"><span data-stu-id="4b104-139">**pszStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4b104-140">Указатель на новую строку значения состояния порта принтера, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="4b104-140">Pointer to a new printer port status value string to set.</span></span> <span data-ttu-id="4b104-141">Используйте этот элемент, если нет подходящего значения состояния в списке для **dwstatus устанавливается**.</span><span class="sxs-lookup"><span data-stu-id="4b104-141">Use this member if there is no suitable status value among those listed for **dwStatus**.</span></span>

</dd> <dt>

<span data-ttu-id="4b104-142">**двсеверити**</span><span class="sxs-lookup"><span data-stu-id="4b104-142">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="4b104-143">Серьезность значения состояния порта.</span><span class="sxs-lookup"><span data-stu-id="4b104-143">The severity of the port status value.</span></span>

<span data-ttu-id="4b104-144">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4b104-144">This member can be one of the following values.</span></span>



| <span data-ttu-id="4b104-145">Значение</span><span class="sxs-lookup"><span data-stu-id="4b104-145">Value</span></span>                       | <span data-ttu-id="4b104-146">Значение</span><span class="sxs-lookup"><span data-stu-id="4b104-146">Meaning</span></span>                                   |
|-----------------------------|-------------------------------------------|
| <span data-ttu-id="4b104-147">\_ \_ Ошибка типа состояния \_ порта</span><span class="sxs-lookup"><span data-stu-id="4b104-147">PORT\_STATUS\_TYPE\_ERROR</span></span>   | <span data-ttu-id="4b104-148">Значение "состояние порта" указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4b104-148">The port status value indicates an error.</span></span> |
| <span data-ttu-id="4b104-149">\_предупреждение о \_ ТИПЕ \_ состояния порта</span><span class="sxs-lookup"><span data-stu-id="4b104-149">PORT\_STATUS\_TYPE\_WARNING</span></span> | <span data-ttu-id="4b104-150">Значение "состояние порта" является предупреждением.</span><span class="sxs-lookup"><span data-stu-id="4b104-150">The port status value is a warning.</span></span>       |
| <span data-ttu-id="4b104-151">\_сведения о \_ ТИПЕ \_ состояния порта</span><span class="sxs-lookup"><span data-stu-id="4b104-151">PORT\_STATUS\_TYPE\_INFO</span></span>    | <span data-ttu-id="4b104-152">Значение состояния порта — информационное.</span><span class="sxs-lookup"><span data-stu-id="4b104-152">The port status value is informational.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b104-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b104-153">Remarks</span></span>

<span data-ttu-id="4b104-154">Если для параметра состояние порта принтера задано значение \_ \_ Ошибка тип состояния порта \_ , диспетчер очереди печати прекращает отправку заданий на порт.</span><span class="sxs-lookup"><span data-stu-id="4b104-154">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="4b104-155">Диспетчер очереди печати не возобновляет отправку заданий в порт, пока не будет выполнен другой вызов [**сетпорт**](setport.md) для очистки состояния.</span><span class="sxs-lookup"><span data-stu-id="4b104-155">The print spooler does not resume sending jobs to the port until another [**SetPort**](setport.md) call is made to clear the status.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b104-156">Требования</span><span class="sxs-lookup"><span data-stu-id="4b104-156">Requirements</span></span>



| <span data-ttu-id="4b104-157">Требование</span><span class="sxs-lookup"><span data-stu-id="4b104-157">Requirement</span></span> | <span data-ttu-id="4b104-158">Значение</span><span class="sxs-lookup"><span data-stu-id="4b104-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b104-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b104-159">Minimum supported client</span></span><br/> | <span data-ttu-id="4b104-160">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b104-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b104-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b104-161">Minimum supported server</span></span><br/> | <span data-ttu-id="4b104-162">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b104-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b104-163">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b104-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b104-164"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b104-164"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4b104-165">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4b104-165">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4b104-166">**\_ \_ Сведения о \_ порте «кто** (Юникод) и **\_ \_ сведения о порте \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4b104-166">**\_PORT\_INFO\_3W** (Unicode) and **\_PORT\_INFO\_3A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="4b104-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b104-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b104-168">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="4b104-168">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4b104-169">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="4b104-169">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4b104-170">**сетпорт**</span><span class="sxs-lookup"><span data-stu-id="4b104-170">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




