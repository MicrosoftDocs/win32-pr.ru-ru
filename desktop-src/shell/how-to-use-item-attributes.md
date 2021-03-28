---
description: Значения флагов СФГАО атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Использование атрибутов элементов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909531"
---
# <a name="how-to-use-item-attributes"></a><span data-ttu-id="43245-103">Использование атрибутов элементов</span><span class="sxs-lookup"><span data-stu-id="43245-103">How to Use Item Attributes</span></span>

<span data-ttu-id="43245-104">Значения флагов [**сфгао**](sfgao.md) атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="43245-104">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="43245-105">Чтобы использовать эту функцию атрибута, добавьте в команду следующие значения **reg \_ DWORD** :</span><span class="sxs-lookup"><span data-stu-id="43245-105">To use this attribute feature, add the following **REG\_DWORD** values under the verb:</span></span>

## <a name="instructions"></a><span data-ttu-id="43245-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="43245-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="43245-107">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="43245-107">Step 1:</span></span>

<span data-ttu-id="43245-108">Значение Аттрибутемаск указывает значение [**сфгао**](sfgao.md) для битовых значений маски для проверки.</span><span class="sxs-lookup"><span data-stu-id="43245-108">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>

### <a name="step-2"></a><span data-ttu-id="43245-109">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="43245-109">Step 2:</span></span>

<span data-ttu-id="43245-110">Значение AttributeValue указывает значение [**сфгао**](sfgao.md) для проверяемых битов.</span><span class="sxs-lookup"><span data-stu-id="43245-110">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="43245-111">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="43245-111">Step 3:</span></span>

<span data-ttu-id="43245-112">Имплиедселектионмодел указывает ноль для глаголов элемента или ненулевое значение для команд в контекстном меню фона.</span><span class="sxs-lookup"><span data-stu-id="43245-112">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

## <a name="remarks"></a><span data-ttu-id="43245-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="43245-113">Remarks</span></span>

<span data-ttu-id="43245-114">В следующем примере записи реестра Аттрибутемаск имеет значение [**сфгао \_ ReadOnly**](sfgao.md) (0x40000).</span><span class="sxs-lookup"><span data-stu-id="43245-114">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



