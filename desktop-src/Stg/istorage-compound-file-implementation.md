---
title: Реализация файла IStorage-Compound
description: Реализация составного файла в IStorage позволяет создавать и администрировать вложенные хранилища и потоки в объекте хранилища, размещенном в объекте составного файла.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- Метод IStorage Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992420"
---
# <a name="istorage-compound-file-implementation"></a>Реализация файла IStorage-Compound

Реализация составного файла в [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) позволяет создавать и администрировать вложенные хранилища и потоки в объекте хранилища, размещенном в объекте составного файла. Чтобы создать объект составного файла и получить указатель **IStorage** , вызовите функцию API [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Чтобы открыть существующий объект составного файла и получить его корневой указатель **IStorage** , вызовите [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Приложения, использующие составное хранилище, должны быть зарегистрированы в \_ \_ корневых СИСТЕМФИЛЕАССОЦИАТИОНС классов hKey \\ и должны предоставлять собственные обработчики свойств. Дополнительные сведения см. в подразделе «регистрация глаголов и других сведений о сопоставлении файлов» раздела [Регистрация приложения](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Назначение

Большинство приложений используют эту реализацию для создания хранилищ и потоков и управления ими.

## <a name="methods"></a>Методы

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: Креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Создает и открывает объект потока с указанным именем, содержащимся в этом объекте хранилища. Длина имени не должна превышать 31 символ (не включая признак конца строки). Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE. Это ограничение составного файла, а ограничение структурированного хранения. Реализация составного файла, предоставленная COM методом [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) , не поддерживает следующие варианты поведения:

-   Флаг СТГМ \_ делетеонрелеасе не поддерживается.
-   Режим транзакций (СТГМ \_ ) не поддерживается для объектов потока.
-   Открытие одного и того же потока более одного раза из одного хранилища не поддерживается. \_ \_ В параметре *грфмоде* должен быть указан флаг общего доступа к общему ресурсу стгм.

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: Опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Открывает существующий объект потока в этом объекте хранилища с использованием режимов доступа, указанных в параметре *грфмоде* . Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE. Это ограничение составного файла, а ограничение структурированного хранения. Реализация составного файла, предоставленная COM методом [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) , не поддерживает следующее поведение:

-   Флаг СТГМ \_ делетеонрелеасе.
-   Режим транзакций (СТГМ \_ ) для потоковых объектов.
-   Открытие одного и того же потока более одного раза из одного хранилища. \_ \_ Необходимо указать флаг монопольного доступа стгм.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: Креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Создает и открывает новый объект хранилища с указанным именем в указанном режиме доступа. Длина имени не должна превышать 31 символ (не включая признак конца строки). Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE. Это ограничение составного файла, а ограничение структурированного хранения. Реализация составного файла, предоставленная COM методом [**IStorage:: креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) , не поддерживает следующее поведение:

-   \_Флаг приоритета стгм для некорневых хранилищ.
-   Открытие одного и того же объекта хранилища более одного раза из одного родительского хранилища. \_ \_ Необходимо указать флаг монопольного доступа стгм.
-   Флаг СТГМ \_ делетеонрелеасе. Если этот флаг указан, функция возвращает STG \_ E \_ инвалидфлаг.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: Опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Открывает существующий объект хранилища с указанным именем в указанном режиме доступа. Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE. Это ограничение составного файла, а ограничение структурированного хранения. Реализация составного файла, предоставленная COM методом [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , не поддерживает следующее поведение:

-   \_Флаг приоритета стгм для некорневых хранилищ.
-   Открытие одного и того же объекта хранилища более одного раза из одного родительского хранилища. \_ \_ Необходимо указать флаг монопольного доступа стгм.
-   Флаг СТГМ \_ делетеонрелеасе. Если этот флаг указан, функция возвращает STG \_ E \_ инвалидфунктион.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Копирует только подхранилища и потоки этого открытого объекта хранилища в другой объект хранилища. Параметр *ргиидексклуде* может иметь значение IID \_ IStream, чтобы копировать только подхранилища или IID \_ IStorage, чтобы копировать только потоки.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: Мовилементто**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Копирует или перемещает подхранилище или поток из этого объекта хранилища в другой объект хранилища.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Гарантирует, что все изменения, вносимые в объект хранилища, открытые в режиме транзакций, отражаются в родительском хранилище. для корневого хранилища отражает изменения в фактическом устройстве; Например, файл на диске. Для объекта корневого хранилища, открытого в режиме прямого доступа, этот метод не действует, кроме сброса всех буферов памяти на диск. Для объектов некорневого хранилища в прямом режиме этот метод не действует.

Реализация составных файлов, предоставляемых COM, использует двухэтапный процесс фиксации, если \_ в параметре *грфкоммитфлагс* не указано значение стгк rewrite. Этот двухэтапный процесс обеспечивает устойчивость данных в случае сбоя операции фиксации. Во-первых, все новые данные записываются в неиспользуемое пространство в базовом файле. При необходимости для файла выделяется новое пространство. После завершения этого шага таблица в файле обновляется с помощью операции записи в один сектор, чтобы указать, что новые данные будут использоваться вместо старого. Старые данные становятся свободным пространством для использования при следующей операции фиксации. Поэтому старые данные доступны и могут быть восстановлены при возникновении ошибки при фиксации изменений. Если \_ указана перезапись стгк, используется однофазная операция фиксации. Дополнительные сведения о флагах режима транзакций см. в разделе [**стгк**](/windows/win32/api/wtypes/ne-wtypes-stgc) Enumeration.

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Отменяет все изменения, внесенные в объект хранилища с момента последней операции фиксации.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: Енумелементс**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Создает и получает указатель на объект перечислителя, который можно использовать для перечисления объектов хранилища и потоков, содержащихся в этом объекте хранилища. Реализация составного файла, предоставляемая моделью COM, создает моментальный снимок этой информации. Поэтому изменения в потоках и хранилищах не отражаются в перечислителе до получения нового перечислителя.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D Естройелемент**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Удаляет указанный элемент (вложенное хранилище или поток) из этого объекта хранилища.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: Ренамилемент**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Переименовывает указанное подхранилище или поток в этом объекте хранилища. Символы от 000 до 01f, служащие как первый символ имени потока/хранилища, зарезервированы для использования OLE. Это ограничение составного файла, а ограничение структурированного хранения.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: Сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Задает время изменения, доступа и создания указанного элемента хранилища. Реализация составных файлов, предоставляемая моделью COM, сохраняет изменения и время изменения для внутренних объектов хранилища. Объекты корневого хранилища поддерживают все, что поддерживается базовой файловой системой (или [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)). Реализация составного файла не поддерживает никакие отметки времени для внутренних потоков. Неподдерживаемые метки времени отмечаются как нулевые, что позволяет вызывающему объекту проверить поддержку.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: Сеткласс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Присваивает указанный идентификатор CLSID этому объекту хранилища.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: Сетстатебитс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Сохраняет до 32 бит информации о состоянии в этом объекте хранилища. Состояние, заданное этим методом, предназначено только для внешнего использования. Реализация составного файла, предоставляемая моделью COM, не выполняет никаких действий в зависимости от состояния.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Извлекает структуру [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) для этого открытого объекта хранилища.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если объект хранилища открыт в простом режиме, использование описанных выше методов будет ограничено. Хранилище находится в простом режиме, если он открыт с помощью \_ простого элемента стгм, указанного в параметре *Грфмоде* функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Дополнительные сведения о хранилищах в простых режимах см. в разделе [**константы стгм**](stgm-constants.md). Если объект хранилища простого режима был получен из функции **стгкреатесторажеекс** , то метод [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) можно вызвать, но метод [**опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) не может. Если объект хранилища простого режима был получен из функции **стгопенсторажеекс** , то метод **опенстреам** можно вызвать, но метод **креатестреам** не может.

Если для создания потока используется объект хранилища простого режима, минимальный размер этого потока обычно составляет 4096 байт. Если в поток записывается меньше данных, размер округляется до 4096 байт.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ограничения реализации составных файлов](structured-storage-interfaces.md)
</dt> <dt>

[**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Метод IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 