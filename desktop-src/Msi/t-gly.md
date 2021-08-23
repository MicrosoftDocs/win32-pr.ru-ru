---
description: сведения о установщик Windows концепциях, начинающихся с буквы T, например с обработкой и преобразованием транзакций.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7148ff7ca92a55698baa8f21e28ee6c4a54d69fd498adaea29c924bc23bc9fda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626714"
---
# <a name="t-windows-installer"></a>T (установщик Windows)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) р [. J K](i-gly.md) L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**обработка транзакций**
</dt> <dd>

Одна или несколько операций обрабатывались в виде одного неделимого целого числа, называемого транзакцией. Все составляющие операции должны быть выполнены, чтобы транзакция была выполнена, в противном случае выполняется откат всех операций в исходное состояние.

</dd> <dt>

<span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Преобразует**
</dt> <dd>

Шаблон различий между двумя [*базами данных установщика*](i-gly.md) , которые можно применить для получения аналогичных изменений в других базах данных. Например, преобразование локализации можно использовать для изменения языка приложения. Дополнительные сведения см. в разделе [слияния и преобразования](merges-and-transforms.md).

</dd> <dt>

<span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**флаги состояния ошибки преобразования**
</dt> <dd>

Набор свойств, используемых для отметки условий ошибок [*преобразования*](/windows). Дополнительные сведения см. в разделе [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> <dt>

<span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**Преобразование флагов проверки**
</dt> <dd>

Набор свойств, используемый для проверки того, что [*Преобразование*](/windows) может быть применено к базе данных. Список этих свойств см. в разделе [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

</dd> </dl>

 

 
