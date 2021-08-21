---
description: Описание использования средства SignTool для подписания файла.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Использование средства SignTool для подписания файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d8e85e8e22f65ccbe8b5f15453b0a0cac34fc27697bad648b1c815f255b10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971474"
---
# <a name="using-signtool-to-sign-a-file"></a>Использование средства SignTool для подписания файла

следующая команда подписывает файл с именем MyControl.exe, используя [*сертификат*](../secgloss/c-gly.md) , хранящийся в файле личных данных Exchange (PFX):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

Следующая команда подписывает файл с помощью сертификата, хранящегося в защищенном паролем файле PFX:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Убедитесь, что пароль правильно защищен.

 

Файл подписывает следующие команды и отметок времени:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Дополнительные сведения о отметке времени для файла после того, как он уже подписан, см. [в разделе Добавление меток времени к ранее подписанным файлам](adding-time-stamps-to-previously-signed-files.md).

 

Следующая команда подписывает файл с помощью сертификата, расположенного в хранилище My, с именем субъекта моей компании Publisher:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

следующая команда подписывает элемент управления ActiveX и предоставляет сведения, отображаемые Internet Explorer, когда пользователю предлагается установить элемент управления:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

Следующая команда подписывает файл с помощью сертификата, сведения о [*закрытом ключе*](../secgloss/p-gly.md) которого защищены аппаратным модулем шифрования. Например, предположим, что сертификат с именем "мой High-Value сертификат" имеет закрытый ключ, установленный в аппаратном модуле шифрования, и сертификат установлен правильно.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

Следующая команда подписывает файл с помощью сертификата, сведения о [*закрытом ключе*](../secgloss/p-gly.md) которого защищены аппаратным модулем шифрования. Для хранилища [*центра сертификации*](../secgloss/c-gly.md) (ЦС) указано хранилище компьютера.

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

Следующая команда подписывает файл с помощью сертификата, хранящегося в файле. Сведения о закрытом ключе защищаются аппаратным модулем шифрования, а [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) и [*контейнер ключей*](../secgloss/k-gly.md) задаются по имени. Эта команда полезна, если сертификат установлен неправильно.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

Средство [SignTool](signtool.md) возвращает текст командной строки, который указывает результат операции подписывания. Кроме того, средство SignTool возвращает нулевой код выхода для успешного выполнения, один для неудачного выполнения и два для выполнения, которые завершились с предупреждениями.

Сведения о проверке подписи файла см. [в разделе Использование средства SignTool для проверки подписи файла](using-signtool-to-verify-a-file-signature.md). Дополнительные сведения о добавлении метки времени, если файл уже подписан, см. в разделе [Добавление меток времени в ранее подписанные файлы](adding-time-stamps-to-previously-signed-files.md). Дополнительные сведения о [SignTool](signtool.md)см. в разделе [SignTool](signtool.md).

 

 
