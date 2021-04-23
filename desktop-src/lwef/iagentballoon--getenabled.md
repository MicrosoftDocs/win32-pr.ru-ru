---
title: Иажентбаллун
description: Иажентбаллун
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332467"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="cb57c-103">Иажентбаллун:: enable</span><span class="sxs-lookup"><span data-stu-id="cb57c-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="cb57c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb57c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="cb57c-105">Извлекает значение свойства [**Enabled**](enabled-property.md) для всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="cb57c-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="cb57c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cb57c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cb57c-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*</span><span class="sxs-lookup"><span data-stu-id="cb57c-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="cb57c-108">Адрес переменной, которая получает **значение true** , если всплывающее сообщение Word включено, и **значение false** , если оно отключено.</span><span class="sxs-lookup"><span data-stu-id="cb57c-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="cb57c-109">Сервер Microsoft Agent автоматически отображает всплывающую подсказку для речевого вывода, если она не отключена.</span><span class="sxs-lookup"><span data-stu-id="cb57c-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="cb57c-110">Всплывающая подсказка может быть отключена для символа в редакторе символов Microsoft Agent или (пользователем) для всех символов на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="cb57c-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="cb57c-111">Если пользователь отключает всплывающую подсказку, клиент не может восстановить его.</span><span class="sxs-lookup"><span data-stu-id="cb57c-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




