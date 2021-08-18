---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3A4C5579-7543-4E0B-921D-BED42C2583D9
title: D (изолированные приложения и параллельные сборки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf0ba858ab8bef37a5b3edc27c64fb19364d582c6b961e3e5f9cc2ac32ef7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142317"
---
# <a name="d-isolated-applications-and-side-by-side-assemblies"></a>D (изолированные приложения и параллельные сборки)

[A](a-sbscs-gly.md) B C D E F [G](g-sbscs-gly.md) р [. J K](i-sbscs-gly.md) L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_def_context_assemblyidentity_gly"></span><span id="_WIN32_DEF_CONTEXT_ASSEMBLYIDENTITY_GLY"></span>**DEF — контекст assemblyIdentity**
</dt> <dd>

Вложенный элемент **assemblyIdentity** , определяющий параллельную сборку, описываемую манифестом. Вложенный элемент **assemblyIdentity** в DEF всегда является первым подэлементом элемента **Assembly** .

</dd> <dt>

<span id="_win32_dll_versioning_conflict_gly"></span><span id="_WIN32_DLL_VERSIONING_CONFLICT_GLY"></span>**Конфликт версий DLL**
</dt> <dd>

Проблема совместимости. Проблемы совместного использования сборок возникают, когда приложение устанавливает версию общей сборки, которая не обратно совместима с ранее установленной версией. Решение о конфликтах версий библиотек DLL заключается в использовании параллельного общего доступа к сборкам и изолированных приложений. при совместном использовании параллельных сборок несколько версий одной и той же Windows сборки могут выполняться одновременно. Разработчики могут выбрать, какую параллельную сборку использовать.

</dd> </dl>

 

 



