---
title: Преобразование строк Юникода и ANSI
description: Microsoft Active Accessibility использует строки в Юникоде, как определено типом данных BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338340"
---
# <a name="converting-unicode-and-ansi-strings"></a>Преобразование строк Юникода и ANSI

Microsoft Active Accessibility использует строки в Юникоде, как определено типом данных **BSTR** . Если приложение не использует строки в Юникоде или вы хотите преобразовать строки для определенных вызовов API, используйте функции Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) и [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для выполнения необходимого преобразования.

Используйте [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для преобразования строки Юникода в строку ANSI. Функция [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) ПРЕОБРАЗУЕТ строку ANSI в строку Юникода.

Используйте [**сисаллокстринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) и [**сисфристринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) для выделения и освобождения типов данных **BSTR** .

Дополнительные сведения об этих строковых функциях см. в разделе ссылки в пакете средств разработки программного обеспечения (SDK) для Windows.

 

 