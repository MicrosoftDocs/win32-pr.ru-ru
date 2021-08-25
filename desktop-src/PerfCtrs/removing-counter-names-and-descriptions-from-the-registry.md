---
description: Средство lodctr удаляет записи реестра, созданные lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Удаление имен и описаний счетчиков из реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c086520f1fb261a0b9850c03f2aee28065a03ee514df277fbf1cae602deed6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962354"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a>Удаление имен и описаний счетчиков из реестра

Средство **lodctr** удаляет записи реестра, созданные **lodctr**. Имя приложения, передаваемое в **lodctr** , должно соответствовать [имени ключа приложения](creating-the-applications-performance-key.md) , созданному в разделе **служб** . Дополнительные сведения о запуске **lodctr** см. в центре справки и поддержки.

## <a name="using-unlodctr"></a>Использование lodctr

Средство **lodctr** ищет первый и последний счетчики и помогает получить значения индексов, используя значения реестра Like, указанные в разделе с ключом **производительности** приложения. Средство **lodctr** использует диапазон значений индекса для удаления текста из **счетчиков** и значений **справки** для каждого идентификатора языка.

Используя значения индекса, **lodctr** вносит в реестр следующие изменения.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

Средство **lodctr** также удаляет **первый счетчик**, **последний счетчик**, **первую справку**, **последнюю справку** и значения **списка объектов** из ключа **производительности** приложения, расположенного в **hKey \_ локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *имя приложения —* \\ **производительность**.

> [!Note]  
> Функция выгрузки **lodctr**, [**унлоадперфкаунтертекстстрингс**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)объявляется в LoadPerf. h и экспортируется из Loadperf.dll. Это позволяет вызывать эту функцию непосредственно из программы удаления.

 

 

 



