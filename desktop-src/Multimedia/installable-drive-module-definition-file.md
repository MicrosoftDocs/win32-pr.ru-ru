---
title: Установочный файл Module-Definition диска
description: Установочный файл Module-Definition диска
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- устанавливаемые драйверы, файлы определения модулей
- устанавливаемые драйверы, DEF файлы
- драйверы нсталлабле, функция Дриверпрок
- Функция Дриверпрок
- файлы определения модуля
- DEF-файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069893"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="191f2-109">Установочный файл Module-Definition диска</span><span class="sxs-lookup"><span data-stu-id="191f2-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="191f2-110">Определение модуля (. DEF). файл устанавливаемого драйвера содержит имя драйвера, экспортирует функцию [дриверпрок](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) и определяет описание драйвера.</span><span class="sxs-lookup"><span data-stu-id="191f2-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="191f2-111">В следующем примере показан типичный файл определения модуля для устанавливаемого драйвера:</span><span class="sxs-lookup"><span data-stu-id="191f2-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="191f2-112">Некоторые приложения установки могут открыть драйвер и получить строку описания для использования при установке драйвера.</span><span class="sxs-lookup"><span data-stu-id="191f2-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="191f2-113">Чтобы сохранить совместимость с этими приложениями установки, строка описания должна иметь следующую форму:</span><span class="sxs-lookup"><span data-stu-id="191f2-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="191f2-114">  *Псевдоним* описания \[ ,*псевдоним* \] ... **:\* \* * текст*</span><span class="sxs-lookup"><span data-stu-id="191f2-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="191f2-115">*Псевдоним* задает уникальное имя драйвера, который приложения могут использовать для открытия драйвера.</span><span class="sxs-lookup"><span data-stu-id="191f2-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="191f2-116">Псевдоним также служит в качестве имени значения, связанного с драйвером в реестре.</span><span class="sxs-lookup"><span data-stu-id="191f2-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="191f2-117">Несколько псевдонимов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="191f2-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="191f2-118">*Текст* описывает назначение драйвера.</span><span class="sxs-lookup"><span data-stu-id="191f2-118">The *text* describes the purpose of the driver.</span></span>

 

 