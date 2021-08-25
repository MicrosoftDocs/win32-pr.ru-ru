---
description: Определяет возможные сертификаты подписи, используемые для цифровых подписей.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Таблица Мсипатчцертификате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39d2bc3a05c8b3fe3f23cd7dce01da36e14ce1f3984f24e827606bbc44c1a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913314"
---
# <a name="msipatchcertificate-table"></a>Таблица Мсипатчцертификате

В таблице Мсипатчцертификате указаны возможные сертификаты для подписи, используемые для цифровых подписей. Таблица Мсипатчцертификате содержит сведения, необходимые для включения [исправления контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md) для приложения.

Таблица Мсипатчцертификате содержит следующие столбцы:



| Столбец               | Type                         | Ключ | Допускает значения NULL |
|----------------------|------------------------------|-----|----------|
| патчцертификате     | [Идентификатор](identifier.md) | Д   | Нет        |
| дигиталцертификате\_ | [Идентификатор](identifier.md) | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>патчцертификате
</dt> <dd>

Уникальный идентификатор этой строки в таблице Мсипатчцертификате.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>дигиталцертификате
</dt> <dd>

Внешний ключ в первом столбце [таблицы мсидигиталцертификате](msidigitalcertificate-table.md). Строка, указанная в таблице Мсидигиталцертификате, содержит двоичное представление сертификата подписи.

</dd> </dl>

## <a name="remarks"></a>Remarks

Исправления всегда оцениваются по таблице Мсипатчцертификате, которая является текущей на момент применения исправления. Исправление может изменить таблицу Мсипатчцертификате, добавляя или удаляя записи. Это позволяет исправить оценку будущих исправлений, которые будут применены позже в последовательности исправлений. В таблице может быть несколько сертификатов, и исправление должно соответствовать по крайней мере одному сертификату, который должен быть применен.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[дисаблелуапатчинг](disableluapatching.md)
</dt> <dt>

[Исправление контроля учетных записей пользователей (UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**мсидисаблелуапатчинг**](msidisableluapatching.md)
</dt> <dt>

[цифровые подписи и установщик Windows](digital-signatures-and-windows-installer.md)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



