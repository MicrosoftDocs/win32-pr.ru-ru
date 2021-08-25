---
Description: Атрибуты файлов — это значения метаданных, которые хранятся в файловой системе на диске и используются системой и доступны для разработчиков с помощью различных API-интерфейсов файлового ввода/вывода.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Константы атрибутов файлов (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: 1dbb3d8e5eb091c47635f78eba9558a0d2262caeb5ce482c7b5bccdc3b237169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050874"
---
# <a name="file-attribute-constants"></a>Константы атрибутов файлов

Атрибуты файлов — это значения метаданных, которые хранятся в файловой системе на диске и используются системой и доступны для разработчиков с помощью различных API-интерфейсов файлового ввода/вывода. Список связанных API и разделов см. в разделе "см. также".

## <a name="example"></a>Пример
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

пример, взятый из [классического примера Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) на GitHub.



| Константа/значение                                                                                                                                                                                                                                                                                                 | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**Файл \_ \_Архив атрибутов**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Файл или каталог, являющийся архивным файлом или каталогом. Приложения обычно используют этот атрибут для пометки файлов для резервного копирования или удаления. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**Файл \_ \_Сжатый атрибут**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Сжатый файл или каталог. Для файла все данные в файле сжимаются. Для каталога по умолчанию используется сжатие для вновь созданных файлов и подкаталогов.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**Файл \_ \_Устройство с атрибутом**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Это значение зарезервировано для использования системой.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**Файл \_ \_Каталог атрибутов**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Маркер, определяющий каталог.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**Файл \_ АТРИБУТ, \_ зашифрованный**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Зашифрованный файл или каталог. Для файла все потоки данных в файле шифруются. Для каталога по умолчанию используется шифрование для вновь созданных файлов и подкаталогов.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**Файл \_ АТРИБУТ \_ Hidden**</dt> <dt>2 (0x2)</dt> </dl>                                                            | Файл или каталог скрыт. Он не включен в обычный список каталогов.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**Файл \_ \_ \_ Поток целостности атрибута**</dt> <dt>32768 (0x8000)</dt> </dl>                      | Для каталога или пользовательского потока данных настроена целостность (поддерживается только на томах ReFS). Он не включен в обычный список каталогов. Параметр целостности сохраняется с файлом, если он переименован. При копировании файла целевой файл будет иметь набор целостности, если в исходном файле или конечном каталоге задана целостность.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** Этот флаг не поддерживается до Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**Файл \_ АТРИБУТ \_ обычного**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Файл, для которого не заданы другие атрибуты. Этот атрибут допустим только при использовании только одного.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**Файл \_ \_ \_ \_ Неиндексируемое содержимое атрибута**</dt> <dt>8192 (0x2000)</dt> </dl>             | Служба индексирования содержимого не должна индексировать файл или каталог.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**Файл \_ АТРИБУТ \_ без \_ очистки \_ данных**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Поток пользовательских данных не считывается средством проверки целостности данных в фоновом режиме (то же самое средство очистки). При задании в каталоге он обеспечивает только наследование. этот флаг поддерживается только для томов дисковые пространства и ReFS. Он не включен в обычный список каталогов.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP:** этот флаг не поддерживается до Windows 8 и Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**Файл \_ АТРИБУТ \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Данные файла недоступны немедленно. Этот атрибут указывает, что данные файла физически перемещаются в автономное хранилище. этот атрибут используется удаленными служба хранилища, которые представляют собой иерархическое программное обеспечение для управления хранилищем. Приложения не должны менять этот атрибут произвольным образом.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**Файл \_ АТРИБУТ \_ ReadOnly**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Файл, который доступен только для чтения. Приложения могут считывать файл, но не могут выполнять запись в него или удалять его. Этот атрибут не учитывается в каталогах. дополнительные сведения см. в статьях [просмотр или изменение системных атрибутов для папок в Windows Server 2003 в Windows XP в Windows Vista или в Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**Файл \_ \_Отзыв атрибута \_ при \_ \_ доступе к данным**</dt> <dt>4194304 (0x400000)</dt> </dl> | Если этот атрибут задан, это означает, что файл или каталог не полностью представлен локально. Для файла это означает, что не все его данные находятся в локальном хранилище (например, оно может быть разреженным, но некоторые данные остаются в удаленном хранилище). Для каталога это означает, что часть содержимого каталога виртуализована из другого расположения. Чтение файла или перечисление каталога будет более дорогим, чем нормальный, например, приведет к тому, что по крайней мере часть содержимого файла или каталога будет получена из удаленного хранилища. Этот бит могут устанавливать только вызывающие объекты в режиме ядра.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**Файл \_ \_Отзыв атрибута \_ для \_ Open**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Этот атрибут отображается только в классах перечисления каталогов ( \_ \_ сведения о каталоге файлов, файлы \_ \_ данных Dir и \_ т. д.). Если этот атрибут задан, это означает, что файл или каталог не имеет физического представления в локальной системе. элемент является виртуальным. Открытие элемента будет более дорогим, чем нормальным, например, приведет к тому, что по крайней мере некоторые из них будут получены из удаленного хранилища.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**Файл \_ \_ \_ Точка повторного анализа атрибута**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Файл или каталог, имеющий связанную точку повторной обработки, или файл, являющийся символьной ссылкой.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**Файл \_ \_Разреженный \_ файл атрибута**</dt> <dt>512 (0x200)</dt> </dl>                                        | Файл, являющийся разреженным файлом.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**Файл \_ \_Система атрибутов**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Файл или каталог, в котором используется операционная система, или используется исключительно.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**Файл \_ \_Временный атрибут**</dt> <dt>256 (0x100)</dt> </dl>                                               | Файл, используемый для временного хранения. Файловые системы не записывают данные обратно в хранилище при наличии достаточного объема кэша, поскольку обычно приложение удаляет временный файл после закрытия этого маркера. В этом случае система может полностью избежать записи данных. В противном случае данные записываются после закрытия маркера.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**Файл \_ АТРИБУТ \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Это значение зарезервировано для использования системой.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>WinNT. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Атрибут Compression](compression-attribute.md)
</dt> <dt>

[Создание и открытие файлов](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**Сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**жетфилеаттрибутестрансактед**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**жетфилеинформатионбихандле**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**жетфилеинформатионбихандликс**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**сетфилеаттрибутестрансактед**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**сетфилеинформатионбихандле**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




