---
description: Определение атрибутов типа файла в реестре.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Определение атрибутов типа файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909548"
---
# <a name="how-to-define-file-type-attributes"></a><span data-ttu-id="762f4-103">Определение атрибутов типа файла</span><span class="sxs-lookup"><span data-stu-id="762f4-103">How to Define File Type Attributes</span></span>

<span data-ttu-id="762f4-104">Назначение атрибутов типа файла связанному идентификатору ProgID позволяет управлять некоторыми аспектами поведения типа файла.</span><span class="sxs-lookup"><span data-stu-id="762f4-104">Assigning file type attributes to an associated ProgID enables you to control some aspects of the file type's behavior.</span></span> <span data-ttu-id="762f4-105">До выхода Windows Vista эти атрибуты могли бы ограничить область, в которой пользователь может использовать вкладку свойств **папки** , для изменения различных аспектов типа файла, таких как значок или команды.</span><span class="sxs-lookup"><span data-stu-id="762f4-105">Prior to Windows Vista, these attributes could enable you to limit the extent to which the user could use the **Folder Options** property tab to modify various aspects of the file type, such as its icon or verbs.</span></span>

<span data-ttu-id="762f4-106">Атрибуты типа файла — это двоичные флаги, указанные в виде **\_ двоичных** значений **reg \_ DWORD** или reg в соответствующем подразделе ProgID типа файла.</span><span class="sxs-lookup"><span data-stu-id="762f4-106">File type attributes are binary flags specified as **REG\_DWORD** or **REG\_BINARY** values in the file type's associated ProgID subkey.</span></span>

<span data-ttu-id="762f4-107">Чтобы назначить атрибуты для типа файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="762f4-107">To assign attributes for a file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="762f4-108">Инструкции</span><span class="sxs-lookup"><span data-stu-id="762f4-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="762f4-109">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="762f4-109">Step 1:</span></span>

<span data-ttu-id="762f4-110">Добавьте запись Едитфлагс в соответствующий подраздел ProgID типа файла.</span><span class="sxs-lookup"><span data-stu-id="762f4-110">Add an EditFlags entry to the file type's associated ProgID subkey.</span></span>

### <a name="step-2"></a><span data-ttu-id="762f4-111">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="762f4-111">Step 2:</span></span>

<span data-ttu-id="762f4-112">Задайте для записи соответствующее значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="762f4-112">Set the entry to the appropriate attribute value.</span></span>

<span data-ttu-id="762f4-113">В следующем примере показаны атрибуты ФТА \_ удаления (0x00000010) и ФТА \_ ноневверб (0x00000020), заданные для типа файла МИП.</span><span class="sxs-lookup"><span data-stu-id="762f4-113">The following example shows the FTA\_NoRemove (0x00000010) and FTA\_NoNewVerb (0x00000020) attributes set for the .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a><span data-ttu-id="762f4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="762f4-114">Remarks</span></span>

<span data-ttu-id="762f4-115">Флаги можно сочетать с логическим или для формирования одного значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="762f4-115">The flags can be combined with a logical OR to form the single attribute value.</span></span>

<span data-ttu-id="762f4-116">Список возможных атрибутов типа файла и их шестнадцатеричных значений, а также дополнительные сведения о программном извлечении и установке этих значений см. в разделе [**филетипеаттрибутефлагс**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span><span class="sxs-lookup"><span data-stu-id="762f4-116">For a list of possible file type attributes and their hexadecimal values, and more details on programmatically retrieving and setting these values, see [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).</span></span>

 

 



