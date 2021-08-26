---
description: начиная с Windows Vista элементы панели управления, входящие в состав Windows, получают каноническое имя, которое можно использовать в вызове API или инструкции командной строки для запуска этого элемента программным способом.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Канонические имена элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebf831bfb1cb86c41a8f97c2bfa041dad836e4b77f8fd233cb94d4a3951c38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943474"
---
# <a name="canonical-names-of-control-panel-items"></a>Канонические имена элементов панели управления

начиная с Windows Vista элементы панели управления, входящие в состав Windows, получают каноническое имя, которое можно использовать в [вызове API или инструкции командной строки](executing-control-panel-items.md) для запуска этого элемента программным способом. начиная с Windows 7 и Windows Server 2008 R2 канонические имена можно использовать в групповой политике для скрытия отдельных элементов панели управления. В этом разделе приводятся сведения для каждого элемента панели управления: каноническое имя, GUID, имя модуля и версии операционной системы, которые распознают каноническое имя.

> [!Note]  
> канонические имена для элементов панели управления не поддерживаются до Windows Vista.

 

-   [Канонические имена панели управления](#control-panel-canonical-names)
-   [Устаревшие канонические имена панели управления](#deprecated-control-panel-canonical-names)
-   [Использование канонических имен в групповая политика](#using-canonical-names-in-local-group-policy)
-   [Замечания](#remarks)

## <a name="control-panel-canonical-names"></a>Канонические имена панели управления

Указывает, что следует помнить при работе со следующими значениями:

-   По определению канонические имена не меняются в зависимости от языка системы; они всегда находятся на английском языке, даже если язык системы отсутствует.
-   Не все элементы панели управления представлены во всех Windows.
-   Некоторые элементы панели управления отображаются только в том случае, если в системе обнаружено правильное оборудование.
-   Сторонние лица также могут добавлять элементы панели управления. Указанные здесь канонические имена предназначены только для элементов панели управления, включенных в Windows.

Ниже перечислены элементы панели управления, доступные в Windows 8.1.

-   [Центр уведомлений](#action-center)
-   [Средства администрирования](#administrative-tools)
-   [Автозапуска](#autoplay)
-   [Биометрические устройства](#biometric-devices)
-   [Шифрование диска BitLocker](#bitlocker-drive-encryption)
-   [Управление цветом](#color-management)
-   [Диспетчер учетных данных](#credential-manager)
-   [Дата и время](#date-and-time)
-   [Программы по умолчанию](#default-programs)
-   [диспетчер устройств](#device-manager)
-   ["Устройства и принтеры"](#devices-and-printers)
-   [Дисплей](#display)
-   [Центр специальных возможностей](#ease-of-access-center)
-   [Семейная безопасность](#family-safety)
-   [История файлов](#file-history)
-   [Свойства папки](#folder-options)
-   [Шрифты](#fonts)
-   [Домашняя группа](#homegroup)
-   [Параметры индексирования](#indexing-options)
-   [Инфракрасная связь](#infrared)
-   [Свойства браузера](#internet-options)
-   [Инициатор iSCSI](#iscsi-initiator)
-   [iSNS-сервер](#isns-server)
-   [Клавиатура](#keyboard)
-   [Параметры расположения](#location-settings)
-   [Мышь](#mouse)
-   [мпиоконфигуратион](#mpioconfiguration)
-   [Центр управления сетями и общим доступом](#network-and-sharing-center)
-   [Значки области уведомлений](#notification-area-icons)
-   [Перо и сенсорный ввод](#pen-and-touch)
-   [Персонализация](#personalization)
-   [Телефон и модем](#phone-and-modem)
-   [Параметры электропитания](#power-options)
-   ["Программы и компоненты",](#programs-and-features)
-   [Восстановление](#recovery)
-   [Регион](#region)
-   [Подключения к рабочим столам и RemoteApp](#remoteapp-and-desktop-connections)
-   [Звук](#sound)
-   [Распознавание речи](#speech-recognition)
-   [Дисковые пространства](#storage-spaces)
-   [Центр синхронизации](#sync-center)
-   [Система](#system)
-   [Параметры планшетных пк](#tablet-pc-settings)
-   [Панель задач и Навигация](#taskbar-and-navigation)
-   [Устранение неполадок](#troubleshooting)
-   [тсаппинсталл](#tsappinstall)
-   [Учетные записи пользователей](#user-accounts)
-   [Windows Anytime Upgrade](#windows-anytime-upgrade)
-   [Защитник Windows](#windows-defender)
-   [Брандмауэр Windows](#windows-firewall)
-   [Центр мобильности Windows](#windows-mobility-center)
-   [Windows To Go](#windows-to-go)
-   [Клиентский компонент Центра обновления Windows](#windows-update)
-   [Рабочие папки](#work-folders)

### <a name="action-center"></a>Центр уведомлений

-   **Каноническое имя**: Microsoft. актионцентер
-   **GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1
-   **Страницы**

    | Имя страницы           | Открытия                      |
    |---------------------|----------------------------|
    | маинтенанцесеттингс | Автоматическое обслуживание      |
    | пажепроблемс        | Отчеты о проблемах            |
    | пажерелиабилитивиев | Монитор надежности        |
    | пажереспонсеарчиве | Архивные сообщения          |
    | pageSettings        | Параметры отчетов о проблемах |

    

     

### <a name="administrative-tools"></a>«Администрирование»

-   **Каноническое имя**: Microsoft. административетулс
-   **GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-22982

### <a name="autoplay"></a>Автозапуск

-   **Каноническое имя**: Microsoft. Автозапуск
-   **GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\autoplay.dll,-1

### <a name="biometric-devices"></a>Биометрические устройства

-   **Каноническое имя**: Microsoft. биометрикдевицес
-   **GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\biocpl.dll,-1

### <a name="bitlocker-drive-encryption"></a>Шифрование диска BitLocker

-   **Каноническое имя**: Microsoft. битлоккердривинкриптион
-   **GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\fvecpl.dll,-1

### <a name="color-management"></a>Управление цветом

-   **Каноническое имя**: Microsoft. колорманажемент
-   **GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\colorcpl.exe,-6

### <a name="credential-manager"></a>Диспетчер учетных данных

-   **Каноническое имя**: Microsoft. кредентиалманажер
-   **GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\Vault.dll,-1
-   **Страницы**

    | Имя страницы                   | Открытия               |
    |-----------------------------|---------------------|
    | ? Селектедваулт = Кредманваулт | учетными данными Windows |

    

     

### <a name="date-and-time"></a>Дата и время

-   **Каноническое имя**: Microsoft. датеандтиме
-   **GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\timedate.cpl,-51
-   **Страницы**

    | Имя страницы | Открытия             |
    |-----------|-------------------|
    | 1         | Дополнительные часы |

    

     

### <a name="default-programs"></a>Программы по умолчанию

-   **Каноническое имя**: Microsoft. дефаултпрограмс
-   **GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\sud.dll,-1
-   **Страницы**

    | Имя страницы          | Открытия                |
    |--------------------|----------------------|
    | пажедефаултпрограм | Установка программ по умолчанию |
    | пажефилеассок      | Задать связи     |

    

     

### <a name="device-manager"></a>Диспетчер устройств

-   **Каноническое имя**: Microsoft. девицеманажер
-   **GUID**: {74246bfc-4c96-11D0-abef-0020af6b0b7a}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\devmgr.dll,-4

### <a name="devices-and-printers"></a>"Устройства и принтеры"

-   **Каноническое имя**: Microsoft. девицесандпринтерс
-   **GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000

### <a name="display"></a>Отображение

-   **Каноническое имя**: Microsoft. дисплей
-   **GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\Display.dll,-1
-   **Страницы**

    | Имя страницы | Открытия             |
    |-----------|-------------------|
    | Параметры  | Разрешение экрана |

    

     

### <a name="ease-of-access-center"></a>Центр специальных возможностей

-   **Каноническое имя**: Microsoft. еасеофакцессцентер
-   **GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10
-   **Страницы**

    | Имя страницы               | Открытия                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | пажееасиертокликк       | Настройка системы для удобной работы с мышью                                        |
    | пажееасиертоси         | Упрощение просмотра компьютера                                     |
    | пажееасиервиссаундс    | Использование текстовых или визуальных вариантов для звуков                          |
    | пажефилтеркэйссеттингс  | Настройка ключей фильтров                                                  |
    | пажекэйбоардеасиертаусе | Настройка системы для удобной работы с клавиатурой                                     |
    | паженомаусеоркэйбоард   | Использование компьютера без мыши или клавиатуры                        |
    | паженовисуал            | Использование компьютера без экрана                                  |
    | пажекуестионскогнитиве  | Получение рекомендаций по упрощению работы с компьютером |
    | пажекуестионсэйесигхт   | Получение рекомендаций по упрощению использования компьютера (эйесигхт)  |

    

     

### <a name="family-safety"></a>Семейная безопасность

-   **Каноническое имя**: Microsoft. паренталконтролс
-   **GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\wpccpl.dll,-100
-   **Страницы**

    | Имя страницы   | Открытия                                  |
    |-------------|----------------------------------------|
    | пажеусерхуб | Выбор пользователя и настройка семейной безопасности |

    

     

### <a name="file-history"></a>История файлов

-   **Каноническое имя**: Microsoft. филехистори
-   **GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}
-   **поддерживаемая ос**: Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\fhcpl.dll,-52
-   В журнал файлов входит более новая версия элемента резервного копирования и восстановления, но каноническое имя этого элемента не переносится в журнал файлов.

### <a name="folder-options"></a>Свойства папки

-   **Каноническое имя**: Microsoft. фолдероптионс
-   **GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-22985

### <a name="fonts"></a>Шрифты

-   **Каноническое имя**: Microsoft. Fonts
-   **GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\FontExt.dll,-8007

### <a name="homegroup"></a>Домашняя группа

-   **Каноническое имя**: Microsoft. Домашняя группа
-   **GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\hgcpl.dll,-1

### <a name="indexing-options"></a>Параметры индексирования

-   **Каноническое имя**: Microsoft. индексингоптионс
-   **GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\srchadmin.dll,-601

### <a name="infrared"></a>Инфракрасная связь

-   **Каноническое имя**: Microsoft. Infrared
-   **GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\irprops.cpl,-1

### <a name="internet-options"></a>Параметры Интернета

-   **Каноническое имя**: Microsoft. интернетоптионс
-   **GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **имя модуля**: @C: \\ Windows \\ System32 \\inetcpl.cpl,-4312
-   **Страницы**

    | Имя страницы | Открытия       |
    |-----------|-------------|
    | 1         | Безопасность    |
    | 2         | Конфиденциальность     |
    | 3         | Содержимое     |
    | 4         | Соединения |
    | 5         | Programs    |
    | 6         | Дополнительно    |

    

     

### <a name="iscsi-initiator"></a>Инициатор iSCSI

-   **Каноническое имя**: Microsoft. исксиинитиатор
-   **GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001

### <a name="isns-server"></a>iSNS-сервер

-   **Каноническое имя**: Microsoft. иснссервер
-   **GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\isnssrv.dll,-5005
-   Этот элемент панели управления будет отображаться только в серверных версиях Windows.

### <a name="keyboard"></a>Клавиатура

-   **Каноническое имя**: Microsoft. Keyboard
-   **GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\main.cpl,-102

### <a name="location-settings"></a>Параметры расположения

-   **Каноническое имя**: Microsoft. локатионсеттингс
-   **GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}
-   **поддерживаемая ос**: Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1

### <a name="mouse"></a>Мышь

-   **Каноническое имя**: Microsoft. Mouse
-   **GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\main.cpl,-100
-   **Страницы**

    | Имя страницы | Открытия           |
    |-----------|-----------------|
    | 1         | Указатели        |
    | 2         | Параметры указателя |
    | 3         | Wheel           |
    | 4         | Оборудование        |

    

     

### <a name="mpioconfiguration"></a>мпиоконфигуратион

-   **Каноническое имя**: Microsoft. мпиоконфигуратион
-   **GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000
-   Этот элемент панели управления будет отображаться только в серверных версиях Windows.

### <a name="network-and-sharing-center"></a>Центр управления сетями и общим доступом

-   **Каноническое имя**: Microsoft. нетворкандшарингцентер
-   **GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\netcenter.dll,-1
-   **Страницы**

    | Имя страницы  | Открытия                     |
    |------------|---------------------------|
    | Дополнительно   | Дополнительные параметры общего доступа |
    | шаремедиа | Параметры потоковой передачи мультимедиа   |

    

     

### <a name="notification-area-icons"></a>Значки области уведомлений

-   **Каноническое имя**: Microsoft. нотификатионареаиконс
-   **GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1

### <a name="pen-and-touch"></a>Перо и сенсорный ввод

-   **Каноническое имя**: Microsoft. пенандтауч
-   **GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103
-   **Страницы**

    | Имя страницы | Открытия       |
    |-----------|-------------|
    | 1         | Жесты      |
    | 2         | Handwriting |

    

     

### <a name="personalization"></a>Personalization

-   **Каноническое имя**: Microsoft. Персонализация
-   **GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\themecpl.dll,-1
-   **Страницы**

    | Имя страницы        | Открытия                |
    |------------------|----------------------|
    | пажеколоризатион | Цвет и внешний вид |
    | пажеваллпапер    | Фон рабочего стола   |

    

     

### <a name="phone-and-modem"></a>Телефон и модем

-   **Каноническое имя**: Microsoft. фонеандмодем
-   **GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\telephon.cpl,-1
-   окно, в котором запускается это значение, задается как "сведения о расположении" в версиях Windows до Windows 8. Пользовательский интерфейс элемента значительно изменился по сравнению с Windows 8.

### <a name="power-options"></a>Параметры электропитания

-   **Каноническое имя**: Microsoft. повероптионс
-   **GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\powercpl.dll,-1
-   **Страницы**

    | Имя страницы          | Открытия              |
    |--------------------|--------------------|
    | пажеглобалсеттингс | Системные настройки    |
    | пажеплансеттингс   | изменить Параметры плана |

    

     

### <a name="programs-and-features"></a>"Программы и компоненты",

-   **Каноническое имя**: Microsoft. програмсандфеатурес
-   **GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\appwiz.cpl,-159
-   **Страницы**

    | Имя страницы                                | Открытия             |
    |------------------------------------------|-------------------|
    | ::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD} | Установленные обновления |

    

     

### <a name="recovery"></a>Восстановление

-   **Каноническое имя**: Microsoft. Recovery
-   **GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\recovery.dll,-101

### <a name="region"></a>Регион

-   **Каноническое имя**: Microsoft. регионандлангуаже
-   **GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\intl.cpl,-1
-   элемент Region и Language, найденный в Windows 7, был разделен на Windows 8. Теперь Microsoft. Регионандлангуаже запускает элемент Region. Чтобы запустить языковой элемент, используйте [Microsoft. Language](#location-settings).
-   **Страницы**

    | Имя страницы | Открытия          |
    |-----------|----------------|
    | 1         | Расположение       |
    | 2         | Административный |

    

     

### <a name="remoteapp-and-desktop-connections"></a>Подключения к рабочим столам и RemoteApp

-   **Каноническое имя**: Microsoft. ремотеаппанддесктопконнектионс
-   **GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300

### <a name="sound"></a>Звук

-   **Каноническое имя**: Microsoft. Sound
-   **GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\mmsys.cpl,-300

### <a name="speech-recognition"></a>Распознавание речи

-   **Каноническое имя**: Microsoft. спичрекогнитион
-   **GUID**: {58E3C745-D971-4081-9034-86E34B30836A}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ System32 \\ Speech \\ спичукс \\speechuxcpl.dll,-1

### <a name="storage-spaces"></a>Дисковые пространства

-   **Каноническое имя**: Microsoft. сторажеспацес
-   **GUID**: {F942C606-0914-47AB-BE56-1321B8035096}
-   **поддерживаемая ос**: Windows 8, Windows 8.1
-   **имя модуля**: @C: \\ Windows \\ System32 \\SpaceControl.dll,-1

### <a name="sync-center"></a>Центр синхронизации

-   **Каноническое имя**: Microsoft. синкцентер
-   **GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000

### <a name="system"></a>Система

-   **Каноническое имя**: Microsoft.SysTEM
-   **GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\systemcpl.dll,-1

### <a name="tablet-pc-settings"></a>Параметры планшетных пк

-   **Каноническое имя**: Microsoft. таблетпксеттингс
-   **GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100

### <a name="taskbar-and-navigation"></a>Панель задач и Навигация

-   **Каноническое имя**: Microsoft. панель задач
-   **GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}
-   **поддерживаемая ос**: Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\shell32.dll,-32517

### <a name="troubleshooting"></a>Устранение неполадок

-   **Каноническое имя**: Microsoft. Устранение неполадок
-   **GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\DiagCpl.dll,-1
-   **Страницы**

    | Имя страницы   | Открытия   |
    |-------------|---------|
    | хисторипаже | Журнал |

    

     

### <a name="tsappinstall"></a>тсаппинсталл

-   **Каноническое имя**: Microsoft. тсаппинсталл
-   **GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}
-   **поддерживаемая ос**: Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001

### <a name="user-accounts"></a>Учетные записи пользователей

-   **Каноническое имя**: Microsoft. UserAccounts
-   **GUID**: {60632754-c523-4b62-b45c-4172da012619}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\usercpl.dll,-1

### <a name="windows-anytime-upgrade"></a>Windows Anytime Upgrade

-   **Каноническое имя**: Microsoft. виндовсанитимеупграде
-   **GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @ $ (ресаурцестринг. \_ \_Путь sys Mod \_ ),-1

### <a name="windows-defender"></a>Защитник Windows

-   **Каноническое имя**: Microsoft. виндовсдефендер
-   **GUID**: {D8559EB9-20C0-410E-Beda-7ED416AECC2A}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **имя модуля**: @% ProgramFiles% \\ Защитник Windows \\MsMpRes.dll,-104

### <a name="windows-firewall"></a>Брандмауэр Windows

-   **Каноническое имя**: Microsoft. брандмауэра Windows
-   **GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **имя модуля**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122
-   **Страницы**

    | Имя страницы         | Открытия        |
    |-------------------|--------------|
    | пажеконфигуреаппс | Разрешенные приложения |

    

     

### <a name="windows-mobility-center"></a>Центр мобильности Windows

-   **Каноническое имя**: Microsoft. мобилитицентер
-   **GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\mblctr.exe,-1002

### <a name="windows-to-go"></a>Windows To Go

-   **Каноническое имя**: Microsoft. портаблеворкспацекреатор
-   **GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}
-   **поддерживаемая ос**: Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\pwcreator.exe,-151

### <a name="windows-update"></a>Центр обновления Windows

-   **Каноническое имя**: Microsoft. windowsupdate
-   **GUID**: {36eef7db-88ad-4e81-AD49-0e313f0c35f8}
-   **поддерживаемая ос**: Windows Vista, Windows 7, Windows 8, Windows 8.1
-   **Имя модуля**: @% systemroot% \\ system32 \\wucltux.dll,-1
-   **Страницы**

    | Имя страницы         | Открытия               |
    |-------------------|---------------------|
    | pageSettings      | Изменить параметры     |
    | пажеупдатехистори | Просмотр журнала обновлений |

    

     

### <a name="work-folders"></a>рабочие папки

-   **Каноническое имя**: Microsoft. воркфолдерс
-   **GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}
-   **поддерживаемая ос**: Windows 8.1
-   **имя модуля**: @C: \\ Windows \\ System32 \\WorkfoldersControl.dll,-1

## <a name="deprecated-control-panel-canonical-names"></a>Устаревшие канонические имена панели управления

ниже приведены канонические имена, которые больше не используются в Windows 8.1 или более поздних версиях. Некоторые из них были удалены полностью. Другие были повторно сопоставлены в следующих ситуациях:

-   Элемент панели управления переименовывается. Переименованному элементу присваивается новое каноническое имя, но сохраняется тот же идентификатор GUID. В этом случае старое каноническое имя запускает переименованный элемент панели управления. Имейте в виду, что запускаемый элемент может не использовать тот же пользовательский интерфейс, что и старая версия этого элемента.
-   Функции одного или нескольких элементов панели управления перемещаются или объединяются в новый элемент. В этом случае старое каноническое имя сопоставляется с наиболее подходящим новым элементом панели управления.

> [!Note]  
> Повторное сопоставление существует для обеспечения обратной совместимости. Не следует использовать устаревшие значения в новом коде.

 



| Устаревшее каноническое имя                                   | Элемент панели управления                | GUID                                   | Примечания                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft. Аддхардваре                                       | Установка оборудования                      | {7A979262-40CE-46ff-AEEE-7884AC3B6136} | Карты в [Microsoft. девицесандпринтерс](#devices-and-printers) начиная с Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. Аудиодевицесандсаундсемес                        | Звук                             | {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D} | Карты в [Microsoft. Sound начиная](#sound) с Windows 7.                                                                                                                                                                                                                                                                                                        |
| Microsoft. Баккупандресторецентер/Microsoft. Баккупандресторе | Центр архивации и восстановления         | {B98A2BEA-7D42-4558-8BD1-832F41BAC6FD} | microsoft. баккупандресторецентер сопоставляется с microsoft. баккупандресторе в Windows 7. Оба параметра удаляются из Windows 8; Вместо этого используйте [Microsoft. филехистори](#file-history) .                                                                                                                                                                                   |
| Microsoft. CardSpace                                         | Windows CardSpace                 | {78CB147A-98EA-4AA6-B0DF-C8681F69341C} | Удалено из Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Десктопгаджетс                                    | Мини-приложения рабочего стола                   | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Удалено из Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Жетпрограмсонлине                                 | Windows Marketplace               | {3e7efb4c-faf1-453d-89eb-56026875ef90} | удалено с Windows 7.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Инфраредоптионс                                   | Инфракрасная связь                          | {A0275511-0E86-4ECA-97C2-ECD8F1221D08} | Карты в [Microsoft. инфракрасная связь](#infrared) на Windows 7.                                                                                                                                                                                                                                                                                                  |
| Microsoft. Language                                          | Язык                          | {BF782CC9-5A52-4A17-806C-2A894FFEEAC5} | удалено из Windows 10, версия 1803                                                                                                                                                                                                                                                                                                                    |
| Microsoft. Локатионандосерсенсорс                           | Расположение и другие датчики        | {E9950154-C418-419e-A90A-20C5287AE24B} | Карты в [Microsoft. локатионсеттингс](#infrared) Windows 8.                                                                                                                                                                                                                                                                                          |
| Microsoft. Пенандинпутдевицес                                | Перо и устройства ввода             | {F82DF8F7-8B9F-442E-A48C-818EA735FF9B} | Карты в [Microsoft. пенандтауч](#pen-and-touch) начиная с Windows 7.                                                                                                                                                                                                                                                                                          |
| Microsoft. Пеопленеарме                                      | Соседние пользователи                    | {5224F545-A443-4859-BA23-7B5A95BDC8EF} | Удалено из Windows 8.                                                                                                                                                                                                                                                                                                                                  |
| Microsoft. Перформанцеинформатионандтулс                    | Сведения о производительности и средства | {78F3955E-3B90-4184-BD14-5397C15F1EFC} | Удалено из Windows 8.1.                                                                                                                                                                                                                                                                                                                                |
| Microsoft. Фонеандмодемоптионс                              | Телефон и модем                   | {40419485-C444-4567-851A-2DD7BFA1684D} | Карты в [Microsoft. фонеандмодем](#phone-and-modem) начиная с Windows 7.                                                                                                                                                                                                                                                                                      |
| Microsoft. Printers                                          | принтеры;                          | {2227A280-3AEA-1069-A2DE-08002B30309D} | Карты в [Microsoft. девицесандпринтерс](#devices-and-printers) начиная с Windows 7.                                                                                                                                                                                                                                                                            |
| Microsoft. Проблемрепортсандсолутионс                        | Отчеты о проблемах и решения     | {ФКФИКАЕ-EE1B-4849-AE50-685DCF7717EC} | Карты в [Microsoft. актионцентер](#action-center) начиная с Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. Регионаландлангуажеоптионс                        | Региональные и языковые параметры     | {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0} | Карты в [Microsoft. регионандлангуаже](#region) начиная с Windows 7. обратите внимание, что по отношению к Windows 8 каждому региону и языку присвоены свои собственные элементы панели управления. В настоящее время Microsoft. Регионаландлангуажеоптионс и Microsoft. Регионандлангуаже открывают элемент региона. Для доступа к элементу языка необходимо использовать [Microsoft. Language](#location-settings) . |
| Microsoft. Секуритицентер                                    | Центр обеспечения безопасности Windows           | {087DA31B-0DD3-4537-8E23-64A18591F88B} | Карты в [Microsoft. актионцентер](#action-center) начиная с Windows 7.                                                                                                                                                                                                                                                                                         |
| Microsoft. Спичрекогнитионоптионс                          | Параметры распознавания речи        | {58E3C745-D971-4081-9034-86E34B30836A} | Карты в [Microsoft. спичрекогнитион](#speech-recognition) начиная с Windows 7.                                                                                                                                                                                                                                                                               |
| Microsoft. Таскбарандстартмену                               | Панель задач и меню "Пуск"            | {0DF44EAA-FF21-4412-828E-260A8728E7F1} | Карты в [Microsoft. панель задач](#speech-recognition) на Windows 8.                                                                                                                                                                                                                                                                                         |
| Microsoft. Велкомецентер                                     | Центр начальной настройки                    | {CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1} | Карты в Microsoft. GettingStarted в Windows 7. Открывает домашнюю страницу панели управления в Windows 8.                                                                                                                                                                                                                                                      |
| Microsoft. Виндовссидебарпропертиес                          | Windows Свойства боковой панели        | {37efd44d-ef8d-41b1-940d-96973a50e9e0} | Карты в Microsoft. десктопгаджетс в Windows 7. Удалено из Windows 8.                                                                                                                                                                                                                                                                                   |
| Microsoft. Виндовссидешов                                   | Windows SideShow                  | {E95A4861-D57A-4be1-AD0F-35267E261739} | нерекомендуемая функция в Windows 8, удалена из Windows 8.1.                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a>Использование канонических имен в локальных групповая политика

начиная с Windows 7 можно использовать канонические имена для ограничения доступа к отдельным элементам панели управления с помощью групповой политики. эта же процедура может использоваться в Windows Vista, но вместо канонического имени необходимо использовать имя модуля.

### <a name="hiding-individual-control-panel-items"></a>Скрытие отдельных элементов панели управления

Используйте этот метод, если требуется отобразить больше элементов панели управления, чем требуется скрыть.

1.  Запустите файл gpedit. msc, чтобы запустить редактор локальных групповых политик. можно также ввести "групповая политика" на начальном экране Windows 8.1 и выбрать пункт **изменить групповую политику** в результатах поиска.
2.  Выберите **Конфигурация пользователя**  >  **Административные шаблоны**  >  **Панель управления**.
3.  Выберите **Скрыть указанные элементы панели управления**.
4.  В открывшемся окне **Скрыть указанные элементы панели управления** щелкните **включено**.
5.  Нажмите кнопку « **Показывать** » на панели «параметры», чтобы отобразить список запрещенных элементов панели управления.
6.  В открывшемся окне **Отображение содержимого** введите каноническое имя в столбец **значение** . При необходимости повторите операцию.
7.  Нажмите **OK**.

### <a name="showing-individual-control-panel-items"></a>Отображение отдельных элементов панели управления

Используйте этот метод, если требуется скрыть больше элементов панели управления, чем требуется отобразить.

1.  Запустите файл gpedit. msc, чтобы запустить редактор локальных групповых политик. можно также ввести "групповая политика" на начальном экране Windows 8.1 и выбрать пункт **изменить групповую политику** в результатах поиска.
2.  Выберите **Конфигурация пользователя**  >  **Административные шаблоны**  >  **Панель управления**.
3.  Выберите **Показывать только указанные элементы панели управления**.
4.  В открывшемся окне **Показывать только указанные элементы панели управления** щелкните **включено**. Это скрывает все элементы на панели управления.
5.  Нажмите кнопку « **Показывать** » на панели «параметры», чтобы отобразить список разрешенных элементов панели управления.
6.  В открывшемся окне **Отображение содержимого** введите каноническое имя в столбец **значение** . При необходимости повторите операцию.
7.  Нажмите **OK**.

Если вы хотите удалить все записи, добавленные в список Показать или скрыть элементы панели управления, вернитесь на экран в шаге 4 и выберите **не настроено** для очистки списка. Если вы хотите хранить записи, но приостановите ограничения, выберите **отключено**.

## <a name="remarks"></a>Remarks

На панели управления могут отображаться элементы, которые не перечислены здесь. эти элементы не являются частью Windows, а добавляются во время установки различных программных и аппаратных средств, таких как Microsoft Office или видеоадаптер. элементы панели управления, не относящиеся к Windows, могут иметь или не иметь канонического имени. Чтобы найти каноническое имя элемента панели управления, не указанного здесь, найдите в реестре следующие пути:

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

Дополнительные сведения, которые могут помочь в обнаружении необходимых идентификаторов CLSID, см. в статьях [Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md) и [Регистрация элементов панели управления DLL](how-to-register-dll-control-panel-item-registration-.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Исполнение элементов панели управления](executing-control-panel-items.md)
</dt> <dt>

[**иопенконтролпанел**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



