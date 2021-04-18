---
description: 'Дополнительные сведения: структура JET_USERDEFINEDDEFAULT'
title: Структура JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693580"
---
# <a name="jet_userdefineddefault-structure"></a>Структура JET_USERDEFINEDDEFAULT


_**Применимо к:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>Структура JET_USERDEFINEDDEFAULT

Структура **JET_USERDEFINEDDEFAULT** задается вместе с JET_bitColumnUserDefinedDefault, чтобы дать новому столбцу значение по умолчанию, которое определяется с помощью обратного вызова. Этот метод можно использовать для реализации вычисленных столбцов.

**Windows XP:** Структура **JET_USERDEFINEDDEFAULT** появилась в Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Элементы

**сзкаллбакк**

Имя экспорта функции, реализующей обратный вызов в формате "функция модуля \! ".

Обратный вызов сохраняется как часть схемы столбца. Фактический исполняемый файл узла и имя экспорта функции должны сохраняться для включения поиска действительного адреса функции во время выполнения.

Имя модуля — это имя двоичного файла узла, содержащего функцию. Имя функции — это имя экспорта для этой функции. Эти два фрагмента информации будут использоваться ядром СУБД в среде выполнения для поиска действительного адреса обратного вызова путем выполнения вызова [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) для имени модуля, за которым следует вызов [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) в имени функции.

Например, если обратный вызов был реализован в библиотеке DLL с именем MyCallback.DLL и эта библиотека DLL хранилась в C: \\ MyApplication, а функция, реализующая обратный вызов, была экспортирована из библиотеки DLL как усердефинеддефаулткаллбакк, то необходимая строка будет иметь вид "C: \\ MyApplication \\MyCallback.DLL\! усердефинеддефаулткаллбакк".

**Примечание**  .  Внедренный " \! " символы в части модуля имени обратного вызова не поддерживаются.

Настоятельно рекомендуется использовать имя обратного вызова, которое не является функцией архитектуры узла. Например, не используйте экспорты, объявленные как STDCALL ( UserDefinedDefaultCallback@32 ), так как это соглашение о вызовах поддерживается только на компьютерах x86. При использовании такого обратного вызова базу данных можно было использовать только на компьютере x86. В этом случае необходимо использовать псевдоним, чтобы сделать независимым от платформы экспорт.

Настоятельно рекомендуется использовать полный путь к имени модуля, реализующего обратный вызов. Если используется относительный путь, процесс, в котором размещается база данных, может быть уязвим для атаки с помощью мошеннического двоичного файла.

Приложение должно передавать ядру СУБД только доверенные обратные вызовы. Ядро СУБД загрузит двоичный файл, чтобы проверить его существование при создании связанного столбца. Если путь к двоичному файлу не проверен или является доверенным, он может атаковать процесс, в котором размещается база данных.

**пбусердата**

Автономный блок определяемых пользователем данных, передаваемый обратному вызову при вызове. Предоставленный блок данных будет сохранен как часть схемы столбца. В результате блок данных должен быть полностью автономным и не может ссылаться на данные, находящиеся за пределами области базы данных.

Если **пбусердата** равен нулю, значение **cbUserData** игнорируется. В этом случае при вызове функции обратного вызова не будут переданы пользовательские данные.

**cbUserData**

См. **пбусердата**.

**сздепендантколумнс**

Зарезервировано для последующего использования.

Этот элемент всегда должен иметь значение NULL.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Юникод) и <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
