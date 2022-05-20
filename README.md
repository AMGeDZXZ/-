
<!---
AMGeDZXZ/AMGeDZXZ is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

"🦅الفار الأذونات مفقودة لإرسال رسائل لـ PRIVATE_GROUP_BOT_API_ID المحدد."                    )
                if entity.default_banned_rights.invite_users:
                    LOGS.info(                        "🦅الفار الأذونات مفقودة لإرسال رسائل لـ PRIVATE_GROUP_BOT_API_ID المحدد."                    )
        except ValueError:
            LOGS.error("🦅تـأكد من فـار المجـموعة  PRIVATE_GROUP_BOT_API_ID.")
        except TypeError:
            LOGS.error(                "🦅لا يمكـن العثور على فار المجموعه PRIVATE_GROUP_BOT_API_ID. تأكد من صحتها."            )
        except Exception as e:
            LOGS.error(                "🦅حدث استثناء عند محاولة التحقق من PRIVATE_GROUP_BOT_API_ID.\n"                + str(e)            )
    else:
        descript = "🦅 لا تحذف هذه المجموعة أو تغير إلى مجموعة (إذا قمت بتغيير المجموعة ، فسيتم فقد كل شيئ .)"
        _, groupid = await create_supergroup(            "مجموعه بوت سورس فـاسـتـر الخاص بك", iqthon, Config.TG_BOT_USERNAME, descript        )
        addgvar("PRIVATE_GROUP_BOT_API_ID", groupid)
        print("🦅 تم إنشاء مجموعة المسـاعدة بنجاح وإضافتها إلى المتغيرات.")
        flag = True
    if PM_LOGGER_GROUP_ID != -100:
        try:
            entity = await iqthon.get_entity(PM_LOGGER_GROUP_ID)
            if not isinstance(entity, types.User) and not entity.creator:
                if entity.default_banned_rights.send_messages:
                    LOGS.info(                        "🦅 الأذونات مفقودة لإرسال رسائل لـ PM_LOGGER_GROUP_ID المحدد."                    )
                if entity.default_banned_rights.invite_users:
                    LOGS.info(                        "🦅الأذونات مفقودة للمستخدمين الإضافيين لـ PM_LOGGER_GROUP_ID المحدد
