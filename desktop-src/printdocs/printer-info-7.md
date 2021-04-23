---
description: В \_ структуре "сведения о принтере 7" \_ указаны сведения о принтере служб каталогов.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Структура PRINTER_INFO_7 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712849"
---
# <a name="printer_info_7-structure"></a><span data-ttu-id="04be8-103">\_Структура сведений о принтере \_ 7</span><span class="sxs-lookup"><span data-stu-id="04be8-103">PRINTER\_INFO\_7 structure</span></span>

<span data-ttu-id="04be8-104">В структуре " **\_ сведения о принтере \_ 7** " указаны сведения о принтере служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="04be8-104">The **PRINTER\_INFO\_7** structure specifies directory services printer information.</span></span> <span data-ttu-id="04be8-105">Используйте эту структуру с функцией [**сетпринтер**](setprinter.md) для публикации данных принтера в службе каталогов (DS), а также для обновления или удаления опубликованных данных принтера из DS.</span><span class="sxs-lookup"><span data-stu-id="04be8-105">Use this structure with the [**SetPrinter**](setprinter.md) function to publish a printer's data in the directory service (DS), or to update or remove a printer's published data from the DS.</span></span> <span data-ttu-id="04be8-106">Используйте эту структуру с функцией [**PrintOut**](getprinter.md) , чтобы определить, опубликован ли принтер в DS.</span><span class="sxs-lookup"><span data-stu-id="04be8-106">Use this structure with the [**GetPrinter**](getprinter.md) function to determine whether a printer is published in the DS.</span></span>

## <a name="syntax"></a><span data-ttu-id="04be8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04be8-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a><span data-ttu-id="04be8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="04be8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04be8-109">**псзобжектгуид**</span><span class="sxs-lookup"><span data-stu-id="04be8-109">**pszObjectGUID**</span></span>
</dt> <dd>

<span data-ttu-id="04be8-110">Указатель на строку с завершающим нулем, содержащую идентификатор GUID объекта очереди печати службы каталогов, связанного с опубликованным принтером.</span><span class="sxs-lookup"><span data-stu-id="04be8-110">A pointer to a null-terminated string containing the GUID of the directory service print queue object associated with a published printer.</span></span> <span data-ttu-id="04be8-111">Чтобы получить этот идентификатор GUID, используйте функцию [**PrintOut**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="04be8-111">Use the [**GetPrinter**](getprinter.md) function to retrieve this GUID.</span></span>

<span data-ttu-id="04be8-112">Перед вызовом [**сетпринтер**](setprinter.md)задайте  для псзобжектгуид **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="04be8-112">Before calling [**SetPrinter**](setprinter.md), set **pszObjectGUID** to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="04be8-113">**двактион**</span><span class="sxs-lookup"><span data-stu-id="04be8-113">**dwAction**</span></span>
</dt> <dd>

<span data-ttu-id="04be8-114">Указывает действие для выполнения функции [**сетпринтер**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="04be8-114">Indicates the action for the [**SetPrinter**](setprinter.md) function to perform.</span></span> <span data-ttu-id="04be8-115">Для функции [**PrintOut**](getprinter.md) этот элемент указывает, опубликован ли указанный принтер.</span><span class="sxs-lookup"><span data-stu-id="04be8-115">For the [**GetPrinter**](getprinter.md) function, this member indicates whether the specified printer is published.</span></span> <span data-ttu-id="04be8-116">Этот элемент может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="04be8-116">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="04be8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="04be8-117">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="04be8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="04be8-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <span data-ttu-id="04be8-119"><dt>**Дспринт \_ ОЖИДАНИе**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-119"><dt>**DSPRINT\_PENDING**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="04be8-120">The [**PrintOut**](getprinter.md): указывает, что система пытается завершить операцию публикации или отмены публикации, запущенную вызовом [**сетпринтер**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="04be8-120">[**GetPrinter**](getprinter.md): Indicates that the system is attempting to complete a publish or unpublish operation started by a [**SetPrinter**](setprinter.md) call.</span></span><br/> <span data-ttu-id="04be8-121">[**Сетпринтер**](setprinter.md): это значение недопустимо.</span><span class="sxs-lookup"><span data-stu-id="04be8-121">[**SetPrinter**](setprinter.md): This value is not valid.</span></span> <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <span data-ttu-id="04be8-122"><dt>**Дспринт \_ Публикация**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-122"><dt>**DSPRINT\_PUBLISH**</dt> <dt>0x00000001</dt></span></span> </dl>       | <span data-ttu-id="04be8-123">[**Сетпринтер**](setprinter.md): публикует данные принтера в DS.</span><span class="sxs-lookup"><span data-stu-id="04be8-123">[**SetPrinter**](setprinter.md): Publishes the printer's data in the DS.</span></span><br/> <span data-ttu-id="04be8-124">The [**PrintOut**](getprinter.md): указывает, что принтер опубликован.</span><span class="sxs-lookup"><span data-stu-id="04be8-124">[**GetPrinter**](getprinter.md): Indicates the printer is published.</span></span> <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <span data-ttu-id="04be8-125"><dt>**Дспринт \_ Повторная публикация**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-125"><dt>**DSPRINT\_REPUBLISH**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="04be8-126">[**Сетпринтер**](setprinter.md): данные DS для принтера не публикуются, а затем публикуются снова, обновляются все свойства на опубликованном принтере.</span><span class="sxs-lookup"><span data-stu-id="04be8-126">[**SetPrinter**](setprinter.md): The DS data for the printer is unpublished and then published again, refreshing all properties in the published printer.</span></span> <span data-ttu-id="04be8-127">Повторная публикация также изменяет идентификатор GUID опубликованного принтера.</span><span class="sxs-lookup"><span data-stu-id="04be8-127">Re-publishing also changes the GUID of the published printer.</span></span><br/> <span data-ttu-id="04be8-128">Метод [**PrintOut**](getprinter.md): никогда не возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="04be8-128">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <span data-ttu-id="04be8-129"><dt>**Дспринт \_ Отмена публикации**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-129"><dt>**DSPRINT\_UNPUBLISH**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="04be8-130">[**Сетпринтер**](setprinter.md): удаляет опубликованные данные принтера из DS.</span><span class="sxs-lookup"><span data-stu-id="04be8-130">[**SetPrinter**](setprinter.md): Removes the printer's published data from the DS.</span></span><br/> <span data-ttu-id="04be8-131">The [**PrintOut**](getprinter.md): указывает, что принтер не опубликован.</span><span class="sxs-lookup"><span data-stu-id="04be8-131">[**GetPrinter**](getprinter.md): Indicates the printer is not published.</span></span> <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <span data-ttu-id="04be8-132"><dt>**Дспринт \_ Обновление**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-132"><dt>**DSPRINT\_UPDATE**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="04be8-133">[**Сетпринтер**](setprinter.md): обновляет опубликованные данные принтера в DS.</span><span class="sxs-lookup"><span data-stu-id="04be8-133">[**SetPrinter**](setprinter.md): Updates the printer's published data in the DS.</span></span><br/> <span data-ttu-id="04be8-134">Метод [**PrintOut**](getprinter.md): никогда не возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="04be8-134">[**GetPrinter**](getprinter.md): Never returns this value.</span></span> <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04be8-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04be8-135">Remarks</span></span>

<span data-ttu-id="04be8-136">Структура **Printer \_ info \_ 7** используется в вызове [**сетпринтер**](setprinter.md) для публикации сведений о принтерах в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="04be8-136">The **PRINTER\_INFO\_7** structure is used in a [**SetPrinter**](setprinter.md) call to publish printer information to the directory service.</span></span> <span data-ttu-id="04be8-137">Опубликованные данные включают все значения и данные для указанного принтера, находящиеся в \_ \_ ключе ДИСПЕТЧЕРА очереди сплдс \_ , \_ ключе драйвера сплдс или сплдс \_ \_ ключах пользователя, созданных [**сетпринтердатаекс**](setprinterdataex.md).</span><span class="sxs-lookup"><span data-stu-id="04be8-137">The published data includes all values and data for the specified printer found under the SPLDS\_SPOOLER\_KEY, SPLDS\_DRIVER\_KEY, or SPLDS\_USER\_KEY keys created by [**SetPrinterDataEx**](setprinterdataex.md).</span></span>

<span data-ttu-id="04be8-138">Для [**сетпринтер**](setprinter.md) *псзобжектгуид* должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="04be8-138">For [**SetPrinter**](setprinter.md), *pszObjectGUID* should be set to **NULL**.</span></span> <span data-ttu-id="04be8-139">Для [](getprinter.md) *псзобжектгуид* возвращает идентификатор GUID объекта очереди печати служб каталогов, связанного с опубликованным принтером.</span><span class="sxs-lookup"><span data-stu-id="04be8-139">For [**GetPrinter**](getprinter.md), *pszObjectGUID* returns the GUID of the directory services print queue object associated with a published printer.</span></span> <span data-ttu-id="04be8-140">Этот идентификатор GUID можно использовать с методами интерфейса Active Directory Services (ADSI) для получения опубликованных данных для принтера.</span><span class="sxs-lookup"><span data-stu-id="04be8-140">You can use this GUID with Active Directory Services Interface (ADSI) methods to retrieve published data for the printer.</span></span> <span data-ttu-id="04be8-141">Однако рекомендуемым методом получения опубликованных данных является вызов функции [**жетпринтердатаекс**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="04be8-141">However, the recommended method for retrieving published data is to call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="04be8-142">Требования</span><span class="sxs-lookup"><span data-stu-id="04be8-142">Requirements</span></span>



| <span data-ttu-id="04be8-143">Требование</span><span class="sxs-lookup"><span data-stu-id="04be8-143">Requirement</span></span> | <span data-ttu-id="04be8-144">Значение</span><span class="sxs-lookup"><span data-stu-id="04be8-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04be8-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04be8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="04be8-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04be8-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04be8-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04be8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="04be8-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04be8-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="04be8-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="04be8-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="04be8-150"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04be8-150"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="04be8-151">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="04be8-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="04be8-152">**\_ \_ Сведения о \_ принтере 7W** (Юникод) и **\_ \_ \_ 7А info** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="04be8-152">**\_PRINTER\_INFO\_7W** (Unicode) and **\_PRINTER\_INFO\_7A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="04be8-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04be8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04be8-154">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="04be8-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="04be8-155">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="04be8-155">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




